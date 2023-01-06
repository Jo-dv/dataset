dataset 주소
* 3일차
  * 예제
    * https://drive.google.com/file/d/1Je5g4vCWihSN6Qw8irjlv8UhUGr-uiSf/view?usp=sharing
* 4 ~ 5일차
  * 참조  
    * train
        * https://drive.google.com/file/d/1co4YGFnm0VPgW-JeIZjLnurNCeauZs6e/view?usp=share_link
    * test
        * https://drive.google.com/file/d/1chKI1BSex81u52DDEkoBAkDri4DcUmKt/view?usp=share_link
  * 캐글 설문  
    * https://drive.google.com/file/d/1cem-XNqPAjqUdA5bIbn1XX9OMqSrS2bv/view?usp=sharing
  * 당뇨병  
    * https://drive.google.com/file/d/1cgTV6grYybWRwpEFfG80RsUHQENh3rxD/view?usp=share_link
  * 코로나  
    * https://drive.google.com/file/d/1cqctUe_n4oXMIrxe6ChaZbLvE4Tv-B2H/view?usp=share_link

```
def cmatrix(target, prediction, title):
    c_matrix = np.zeros([2, 2]).astype(np.int64)

    for i in range(target.shape[0]):
        idx_target = np.abs(target[i].astype(int) - 1)
        idx_output = np.abs(prediction[i].astype(int) - 1)

        c_matrix[idx_target, idx_output] += 1

    c_matrix_frame = pd.DataFrame(c_matrix, index=['Actual(P)', 'Actual(N)'], columns=['Predicted(P)', 'Predicted(N)'])

    plt.figure(figsize=(4, 3))
    plt.title(title)
    sns.heatmap(c_matrix_frame, annot = True, fmt = 'd',cmap = 'Reds')
    plt.xlabel('Predicted')
    plt.ylabel('Actual')
    plt.xticks([0.5, 1.5],['P', 'N'])
    plt.yticks([0.5, 1.5],['P', 'N'])
    plt.show()
    
    TP = c_matrix[0][0]
    FP = c_matrix[1][0]
    FN = c_matrix[0][1]
    TN = c_matrix[1][1]
    
    Accuracy = (TP + TN) / (TP + TN + FP + FN)
    Precision = TP / (TP + FP)
    Recall = TP / (TP + FN)
    Specificity = TN / (TN + FP)
    F1_score = 2 * (Precision * Recall) / (Precision + Recall)
    print('Accuracy:', Accuracy)
    print('Precision:', Precision)
    print('Recall:', Recall)
    print('Specificity:', Specificity)
    print('F1_score:', F1_score)
```


    Genel Q-learning Algoritması:
        Q(s, a) += alpha * (reward(s,a) + gamma * max(Q(s') - Q(s,a))
    DQN:
        target = reward(s,a) + gamma * max(Q(s')
            

DQN algoritmasında belirli bir durum için s, Q(s,·; θ) eylem değerlerinin çıktılarını veren çok katmanlı bir sinir ağıdır. Bu vektörde θ ağın parametreleridir. Bir n boyutlu durum alanı ve m eylemlerini içeren bir eylem alanı için, sinir ağı R_n'den R_m'ye bir fonksiyondur. DQN algoritmasının iki önemli bileşeni, bir hedef ağın kullanımı ve deneyim tekrarının kullanılmasıdır.


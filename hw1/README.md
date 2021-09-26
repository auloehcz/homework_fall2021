### Section 1 (Behavior Cloning)
Ant command for problem 1.2:

```
python cs285/scripts/run_hw1.py \
	--expert_policy_file cs285/policies/experts/Ant.pkl \
	--env_name Ant-v2 --exp_name bc_ant --n_iter 1 \
	--expert_data cs285/expert_data/expert_data_Ant-v2.pkl \
	--video_log_freq -1 --ep_len 1000 --batch_size 10000 \
    --eval_batch_size 10000 --train_batch_size 1000 \
```
Hopper command for problem 1.2:
```
python cs285/scripts/run_hw1.py \
	--expert_policy_file cs285/policies/experts/Hopper.pkl \
	--env_name Hopper-v2 --exp_name bc_hopper --n_iter 1 \
	--expert_data cs285/expert_data/expert_data_NHopper-v2.pkl \
	--video_log_freq -1 --ep_len 1000 --batch_size 10000 \
    --eval_batch_size 10000 --train_batch_size 1000 \
```

Hopper command for problem 1.3, where you have to fill in `<INSERT NUMBER HERE>` with numbers 1 through 8:
```
python cs285/scripts/run_hw1.py \
	--expert_policy_file cs285/policies/experts/Hopper.pkl \
	--env_name Hopper-v2 --exp_name bc_hopper --n_iter 1 \
	--expert_data cs285/expert_data/expert_data_Hopper-v2.pkl \
	--video_log_freq -1 --ep_len 1000 --batch_size 10000 \
    --eval_batch_size 10000 --train_batch_size 1000 \
    --n_layers <INSERT NUMBER HERE>
```
### Section 2 (DAgger)
Command for section 1:
(Note the `--do_dagger` flag, and the higher value for `n_iter`)

```
python cs285/scripts/run_hw1.py \
    --expert_policy_file cs285/policies/experts/Ant.pkl \
    --env_name Ant-v2 --exp_name dagger_ant --n_iter 10 \
    --do_dagger --expert_data cs285/expert_data/expert_data_Ant-v2.pkl \
	--video_log_freq -1 --ep_len 1000 --batch_size 10000 \
    --eval_batch_size 10000 --train_batch_size 1000 \
    --n_layers 5
```

```
python cs285/scripts/run_hw1.py \
    --expert_policy_file cs285/policies/experts/Hopper.pkl \
    --env_name Hopper-v2 --exp_name dagger_hopper --n_iter 10 \
    --do_dagger --expert_data cs285/expert_data/expert_data_Hopper-v2.pkl \
	--video_log_freq -1 --ep_len 1000 --batch_size 10000 \
    --eval_batch_size 10000 --train_batch_size 1000 \
    --n_layers 5
```

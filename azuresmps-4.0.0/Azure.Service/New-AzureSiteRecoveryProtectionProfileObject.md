---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: 63274c772c6085fc8c491557851673a38056aa77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075891"
---
# <span data-ttu-id="6051d-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="6051d-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="6051d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6051d-102">SYNOPSIS</span></span>
<span data-ttu-id="6051d-103">Создание объекта профиля защиты для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="6051d-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="6051d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6051d-104">SYNTAX</span></span>

### <span data-ttu-id="6051d-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6051d-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="6051d-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="6051d-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6051d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6051d-107">DESCRIPTION</span></span>
<span data-ttu-id="6051d-108">Командлет **New-AzureSiteRecoveryProtectionProfileObject** создает объект профиля защиты для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="6051d-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="6051d-109">Этот командлет создает объект **ASRProtectionProfile** для использования с другими командлетами.</span><span class="sxs-lookup"><span data-stu-id="6051d-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="6051d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6051d-110">EXAMPLES</span></span>

### <span data-ttu-id="6051d-111">Пример 1: Создание профиля защиты</span><span class="sxs-lookup"><span data-stu-id="6051d-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="6051d-112">Эта команда создает объект профиля защиты.</span><span class="sxs-lookup"><span data-stu-id="6051d-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="6051d-113">Пример 2: Создание профиля защиты для поставщика HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="6051d-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="6051d-114">Эта команда создает профиль защиты для поставщика HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="6051d-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="6051d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6051d-115">PARAMETERS</span></span>

### <span data-ttu-id="6051d-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="6051d-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="6051d-117">Указывает на то, что профиль защиты включает удаление сущностей реплики.</span><span class="sxs-lookup"><span data-stu-id="6051d-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="6051d-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="6051d-119">Указывает частоту (в часах) для моментальных снимков, учитывающих приложение.</span><span class="sxs-lookup"><span data-stu-id="6051d-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-120">-Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="6051d-120">-Authentication</span></span>
<span data-ttu-id="6051d-121">Указывает тип проверки подлинности для использования.</span><span class="sxs-lookup"><span data-stu-id="6051d-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="6051d-122">Допустимые значения этого параметра: Certificate и Kerberos.</span><span class="sxs-lookup"><span data-stu-id="6051d-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="6051d-123">-CompressionEnabled</span></span>
<span data-ttu-id="6051d-124">Указывает на то, что профиль защиты обеспечивает сжатие.</span><span class="sxs-lookup"><span data-stu-id="6051d-124">Indicates that the protection profile enables compression.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6051d-125">-Force</span></span>
<span data-ttu-id="6051d-126">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="6051d-126">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6051d-127">-Name</span></span>
<span data-ttu-id="6051d-128">Задает имя профиля защиты.</span><span class="sxs-lookup"><span data-stu-id="6051d-128">Specifies a name for the protection profile.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="6051d-129">-Profile</span></span>
<span data-ttu-id="6051d-130">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="6051d-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6051d-131">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6051d-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="6051d-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="6051d-133">Указывает имя учетной записи хранения Azure, на которой будет храниться сущность реплики Azure.</span><span class="sxs-lookup"><span data-stu-id="6051d-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="6051d-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="6051d-135">Указывает идентификатор подписки Azure для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="6051d-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="6051d-136">Этот параметр указывает на учетную запись, на которой будет храниться сущность реплики Azure.</span><span class="sxs-lookup"><span data-stu-id="6051d-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="6051d-137">-RecoveryPoints</span></span>
<span data-ttu-id="6051d-138">Задает количество часов в часах для хранения точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="6051d-138">Specifies the number of hours to retain recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="6051d-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="6051d-140">Указывает интервал частот (в секундах) для репликации.</span><span class="sxs-lookup"><span data-stu-id="6051d-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="6051d-141">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6051d-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6051d-142">30</span><span class="sxs-lookup"><span data-stu-id="6051d-142">30</span></span> 
- <span data-ttu-id="6051d-143">300</span><span class="sxs-lookup"><span data-stu-id="6051d-143">300</span></span> 
- <span data-ttu-id="6051d-144">900</span><span class="sxs-lookup"><span data-stu-id="6051d-144">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="6051d-145">-ReplicationMethod</span></span>
<span data-ttu-id="6051d-146">Указывает метод репликации.</span><span class="sxs-lookup"><span data-stu-id="6051d-146">Specifies the replication method.</span></span> <span data-ttu-id="6051d-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="6051d-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="6051d-148">Онлайн.</span><span class="sxs-lookup"><span data-stu-id="6051d-148">Online.</span></span>
<span data-ttu-id="6051d-149">Репликация по сети.</span><span class="sxs-lookup"><span data-stu-id="6051d-149">Replication over the network.</span></span>
- <span data-ttu-id="6051d-150">Доступ.</span><span class="sxs-lookup"><span data-stu-id="6051d-150">Offline.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="6051d-151">-ReplicationPort</span></span>
<span data-ttu-id="6051d-152">Указывает номер порта, на котором выполняется репликация.</span><span class="sxs-lookup"><span data-stu-id="6051d-152">Specifies the number of the port on which the replication occurs.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="6051d-153">-ReplicationProvider</span></span>
<span data-ttu-id="6051d-154">Указывает тип поставщика репликации.</span><span class="sxs-lookup"><span data-stu-id="6051d-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="6051d-155">Допустимые значения этого параметра: HyperVReplica и HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="6051d-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="6051d-156">-ReplicationStartTime</span></span>
<span data-ttu-id="6051d-157">Задает время начала репликации.</span><span class="sxs-lookup"><span data-stu-id="6051d-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="6051d-158">Укажите время в течение 24 часов после начала задания.</span><span class="sxs-lookup"><span data-stu-id="6051d-158">Specify a time within 24 hours after you start the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6051d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6051d-159">CommonParameters</span></span>
<span data-ttu-id="6051d-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6051d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6051d-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6051d-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6051d-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6051d-162">INPUTS</span></span>

## <span data-ttu-id="6051d-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6051d-163">OUTPUTS</span></span>

## <span data-ttu-id="6051d-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="6051d-164">NOTES</span></span>

## <span data-ttu-id="6051d-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6051d-165">RELATED LINKS</span></span>

[<span data-ttu-id="6051d-166">Командлеты служб Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="6051d-166">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)



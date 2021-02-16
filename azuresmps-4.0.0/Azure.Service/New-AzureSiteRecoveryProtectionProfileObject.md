---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 853D5585-2A92-4B65-BA8C-EC06BEE8C237
online version: ''
schema: 2.0.0
ms.openlocfilehash: d7681631d98f80def1076a04ab57f1774bad245c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403652"
---
# <span data-ttu-id="19269-101">New-AzureSiteRecoveryProtectionProfileObject</span><span class="sxs-lookup"><span data-stu-id="19269-101">New-AzureSiteRecoveryProtectionProfileObject</span></span>

## <span data-ttu-id="19269-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19269-102">SYNOPSIS</span></span>
<span data-ttu-id="19269-103">Создание объекта профиля защиты от восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="19269-103">Creates a Site Recovery protection profile object.</span></span>

## <span data-ttu-id="19269-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19269-104">SYNTAX</span></span>

### <span data-ttu-id="19269-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19269-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 -RecoveryAzureSubscription <String> -RecoveryAzureStorageAccount <String>
 -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="19269-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="19269-106">EnterpriseToEnterprise</span></span>
```
New-AzureSiteRecoveryProtectionProfileObject [-Name <String>] -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String> [-RecoveryPoints <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-CompressionEnabled] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-AllowReplicaDeletion] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="19269-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19269-107">DESCRIPTION</span></span>
<span data-ttu-id="19269-108">С **его использованием** создается объект профиля защиты от восстановления сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="19269-108">The **New-AzureSiteRecoveryProtectionProfileObject** cmdlet creates an Azure Site Recovery protection profile object.</span></span>
<span data-ttu-id="19269-109">Этот cmdlet создает объект **ASRProtectionProfile** для использования с другими.</span><span class="sxs-lookup"><span data-stu-id="19269-109">This cmdlet creates an **ASRProtectionProfile** object to use with other cmdlets.</span></span>

## <span data-ttu-id="19269-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19269-110">EXAMPLES</span></span>

### <span data-ttu-id="19269-111">Пример 1. Создание профиля защиты</span><span class="sxs-lookup"><span data-stu-id="19269-111">Example 1: Create a protection profile</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -ReplicationProvider "HyperVReplica" -AllowReplicaDeletion -ApplicationConsistentSnapshotFrequencyInHours 1 -CompressionEnabled -RecoveryPoints 2 -ReplicationFrequencyInSeconds 30 -ReplicationMethod "Online" -ReplicationPort 8085 -ReplicationStartTime 1
Name                                     : 
ID                                       : 
ReplicationProvider                      : HyperVReplica
HyperVReplicaProviderSettingsObject      : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaProviderSettings
HyperVReplicaAzureProviderSettingsObject :
```

<span data-ttu-id="19269-112">Эта команда создает объект профиля защиты.</span><span class="sxs-lookup"><span data-stu-id="19269-112">This command creates a protection profile object.</span></span>

### <span data-ttu-id="19269-113">Пример 2. Создание профиля защиты для поставщика HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="19269-113">Example 2: Create a protection profile for HyperVReplicaAzure provider</span></span>
```
PS C:\> New-AzureSiteRecoveryProtectionProfileObject -Name "ProtectionProfile" -ReplicationProvider "HyperVReplicaAzure" -RecoveryAzureSubscription "cb53d0c3-bd59-4721-89bc-06916a9147ef" -RecoveryAzureStorageAccount "Contoso01" -ReplicationFrequencyInSeconds 30 -RecoveryPoints 1 -Force
Name                                     : ProtectionProfile
ID                                       : 
ReplicationProvider                      : HyperVReplicaAzure
HyperVReplicaProviderSettingsObject      : 
HyperVReplicaAzureProviderSettingsObject : Microsoft.Azure.Portal.RecoveryServices.Models.Common.HyperVReplicaAzureProviderSettings
```

<span data-ttu-id="19269-114">Эта команда создает профиль защиты для поставщика HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="19269-114">This command creates a protection profile for a HyperVReplicaAzure provider.</span></span>

## <span data-ttu-id="19269-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19269-115">PARAMETERS</span></span>

### <span data-ttu-id="19269-116">-AllowReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="19269-116">-AllowReplicaDeletion</span></span>
<span data-ttu-id="19269-117">Указывает на то, что профиль защиты позволяет удалять репликируемые объекты.</span><span class="sxs-lookup"><span data-stu-id="19269-117">Indicates that the protection profile enables deletion of replica entities.</span></span>

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

### <span data-ttu-id="19269-118">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="19269-118">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="19269-119">Определяет частоту в часах для согласованных моментальных снимков приложения.</span><span class="sxs-lookup"><span data-stu-id="19269-119">Specifies the frequency, in hours, for application consistent snapshots.</span></span>

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

### <span data-ttu-id="19269-120">-Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="19269-120">-Authentication</span></span>
<span data-ttu-id="19269-121">Определяет тип проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="19269-121">Specifies the type of authentication to use.</span></span>
<span data-ttu-id="19269-122">Допустимыми значениями для этого параметра являются Сертификат и Kerberos.</span><span class="sxs-lookup"><span data-stu-id="19269-122">The acceptable values for this parameter are: Certificate and Kerberos.</span></span>

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

### <span data-ttu-id="19269-123">-CompressionEnabled</span><span class="sxs-lookup"><span data-stu-id="19269-123">-CompressionEnabled</span></span>
<span data-ttu-id="19269-124">Указывает на то, что профиль защиты обеспечивает сжатие.</span><span class="sxs-lookup"><span data-stu-id="19269-124">Indicates that the protection profile enables compression.</span></span>

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

### <span data-ttu-id="19269-125">-Force</span><span class="sxs-lookup"><span data-stu-id="19269-125">-Force</span></span>
<span data-ttu-id="19269-126">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="19269-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="19269-127">-Name</span><span class="sxs-lookup"><span data-stu-id="19269-127">-Name</span></span>
<span data-ttu-id="19269-128">Указывает имя профиля защиты.</span><span class="sxs-lookup"><span data-stu-id="19269-128">Specifies a name for the protection profile.</span></span>

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

### <span data-ttu-id="19269-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="19269-129">-Profile</span></span>
<span data-ttu-id="19269-130">Определяет профиль Azure, для которого читается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19269-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="19269-131">Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="19269-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="19269-132">-RecoveryAzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="19269-132">-RecoveryAzureStorageAccount</span></span>
<span data-ttu-id="19269-133">Указывает имя учетной записи хранилища Azure, на которой будет храниться объект репликации Azure.</span><span class="sxs-lookup"><span data-stu-id="19269-133">Specifies the name of an Azure Storage account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="19269-134">-RecoveryAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="19269-134">-RecoveryAzureSubscription</span></span>
<span data-ttu-id="19269-135">Определяет ИД подписки Azure для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="19269-135">Specifies the ID for an Azure Subscription for a storage account.</span></span>
<span data-ttu-id="19269-136">Этот параметр ссылается на учетную запись, для которой нужно сохранить объект репликации Azure.</span><span class="sxs-lookup"><span data-stu-id="19269-136">This parameter refers to the account on which to store the Azure replica entity.</span></span>

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

### <span data-ttu-id="19269-137">-RecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="19269-137">-RecoveryPoints</span></span>
<span data-ttu-id="19269-138">Количество часов для сохранения точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="19269-138">Specifies the number of hours to retain recovery points.</span></span>

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

### <span data-ttu-id="19269-139">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="19269-139">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="19269-140">Определяет частоту репликации (в секундах).</span><span class="sxs-lookup"><span data-stu-id="19269-140">Specifies the frequency interval, in seconds, for replication.</span></span> <span data-ttu-id="19269-141">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="19269-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19269-142">30</span><span class="sxs-lookup"><span data-stu-id="19269-142">30</span></span> 
- <span data-ttu-id="19269-143">300</span><span class="sxs-lookup"><span data-stu-id="19269-143">300</span></span> 
- <span data-ttu-id="19269-144">900</span><span class="sxs-lookup"><span data-stu-id="19269-144">900</span></span>

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

### <span data-ttu-id="19269-145">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="19269-145">-ReplicationMethod</span></span>
<span data-ttu-id="19269-146">Определяет способ репликации.</span><span class="sxs-lookup"><span data-stu-id="19269-146">Specifies the replication method.</span></span> <span data-ttu-id="19269-147">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="19269-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19269-148">Онлайн.</span><span class="sxs-lookup"><span data-stu-id="19269-148">Online.</span></span>
<span data-ttu-id="19269-149">Репликация по сети.</span><span class="sxs-lookup"><span data-stu-id="19269-149">Replication over the network.</span></span>
- <span data-ttu-id="19269-150">Не в сети.</span><span class="sxs-lookup"><span data-stu-id="19269-150">Offline.</span></span>

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

### <span data-ttu-id="19269-151">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="19269-151">-ReplicationPort</span></span>
<span data-ttu-id="19269-152">Определяет номер порта, для которого происходит репликация.</span><span class="sxs-lookup"><span data-stu-id="19269-152">Specifies the number of the port on which the replication occurs.</span></span>

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

### <span data-ttu-id="19269-153">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="19269-153">-ReplicationProvider</span></span>
<span data-ttu-id="19269-154">Определяет тип поставщика репликации.</span><span class="sxs-lookup"><span data-stu-id="19269-154">Specifies the type of replication provider.</span></span> <span data-ttu-id="19269-155">Допустимые значения этого параметра: HyperVReplica и HyperVReplicaAzure.</span><span class="sxs-lookup"><span data-stu-id="19269-155">The acceptable values for this parameter are: HyperVReplica and HyperVReplicaAzure.</span></span>

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

### <span data-ttu-id="19269-156">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="19269-156">-ReplicationStartTime</span></span>
<span data-ttu-id="19269-157">Время начала репликации.</span><span class="sxs-lookup"><span data-stu-id="19269-157">Specifies the start time of the replication.</span></span>
<span data-ttu-id="19269-158">Укажите время в течение 24 часов после начала работы.</span><span class="sxs-lookup"><span data-stu-id="19269-158">Specify a time within 24 hours after you start the job.</span></span>

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

### <span data-ttu-id="19269-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19269-159">CommonParameters</span></span>
<span data-ttu-id="19269-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19269-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19269-161">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19269-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19269-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19269-162">INPUTS</span></span>

## <span data-ttu-id="19269-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19269-163">OUTPUTS</span></span>

## <span data-ttu-id="19269-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19269-164">NOTES</span></span>

## <span data-ttu-id="19269-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19269-165">RELATED LINKS</span></span>





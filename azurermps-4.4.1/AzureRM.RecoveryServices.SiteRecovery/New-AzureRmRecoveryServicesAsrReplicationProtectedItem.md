---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: cec626d48e5daebe04ad33b13713b56c96e27b17
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562268"
---
# <span data-ttu-id="394f1-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="394f1-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="394f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="394f1-102">SYNOPSIS</span></span>
<span data-ttu-id="394f1-103">Включает репликацию для защищенного элемента ASR путем создания элемента, защищенного репликацией</span><span class="sxs-lookup"><span data-stu-id="394f1-103">Enables replication for an ASR protectable item by creating a replication protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="394f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="394f1-104">SYNTAX</span></span>

### <span data-ttu-id="394f1-105">Отключение (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="394f1-105">DisableDR (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="394f1-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="394f1-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="394f1-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="394f1-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="394f1-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="394f1-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> -RecoveryResourceGroupId <String> [-WaitForCompletion] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="394f1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="394f1-109">DESCRIPTION</span></span>
<span data-ttu-id="394f1-110">Командлет **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** создает новый элемент, защищенный репликацией.</span><span class="sxs-lookup"><span data-stu-id="394f1-110">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="394f1-111">Используйте этот командлет, чтобы включить репликацию для защищенного элемента ASR.</span><span class="sxs-lookup"><span data-stu-id="394f1-111">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="394f1-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="394f1-112">EXAMPLES</span></span>

### <span data-ttu-id="394f1-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="394f1-113">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="394f1-114">Запускает операцию создания защищенного элемента репликации для указанного защищенного элемента ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="394f1-114">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="394f1-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="394f1-115">PARAMETERS</span></span>

### <span data-ttu-id="394f1-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="394f1-116">-Name</span></span>
<span data-ttu-id="394f1-117">Задает имя для элемента, защищенного репликацией ASR.</span><span class="sxs-lookup"><span data-stu-id="394f1-117">Specifies a name for the ASR replication protected item.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394f1-118">-OS</span><span class="sxs-lookup"><span data-stu-id="394f1-118">-OS</span></span>
<span data-ttu-id="394f1-119">Указывает семейство операционной системы.</span><span class="sxs-lookup"><span data-stu-id="394f1-119">Specifies the operating system family.</span></span>
<span data-ttu-id="394f1-120">Допустимые значения этого параметра: Windows или Linux.</span><span class="sxs-lookup"><span data-stu-id="394f1-120">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394f1-121">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="394f1-121">-OSDiskName</span></span>
<span data-ttu-id="394f1-122">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="394f1-122">Specifies the name of the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394f1-123">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="394f1-123">-ProtectableItem</span></span>
<span data-ttu-id="394f1-124">Указывает объект защищенного элемента ASR, для которого включена репликация.</span><span class="sxs-lookup"><span data-stu-id="394f1-124">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="394f1-125">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="394f1-125">-ProtectionContainerMapping</span></span>
<span data-ttu-id="394f1-126">Указывает объект сопоставления контейнера защиты ASR, соответствующий политике репликации, которая должна использоваться для репликации.</span><span class="sxs-lookup"><span data-stu-id="394f1-126">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394f1-127">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="394f1-127">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="394f1-128">Указывает идентификатор учетной записи хранения Azure, на которую должна выполняться репликация.</span><span class="sxs-lookup"><span data-stu-id="394f1-128">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394f1-129">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="394f1-129">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="394f1-130">Указывает идентификатор ARM для группы ресурсов, в которой виртуальная машина будет создана в случае отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="394f1-130">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394f1-131">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="394f1-131">-WaitForCompletion</span></span>
<span data-ttu-id="394f1-132">Указывает, что перед возвратом командлет должен дождаться завершения операции.</span><span class="sxs-lookup"><span data-stu-id="394f1-132">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="394f1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="394f1-133">-Confirm</span></span>
<span data-ttu-id="394f1-134">Запрашивает подтверждение перед запуском операции.</span><span class="sxs-lookup"><span data-stu-id="394f1-134">Prompts  for confirmation before starting the operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394f1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="394f1-135">-WhatIf</span></span>
<span data-ttu-id="394f1-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="394f1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="394f1-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="394f1-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="394f1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="394f1-138">CommonParameters</span></span>
<span data-ttu-id="394f1-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="394f1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="394f1-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="394f1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="394f1-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="394f1-141">INPUTS</span></span>

### <span data-ttu-id="394f1-142">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="394f1-142">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="394f1-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="394f1-143">OUTPUTS</span></span>

### <span data-ttu-id="394f1-144">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="394f1-144">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="394f1-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="394f1-145">NOTES</span></span>

## <span data-ttu-id="394f1-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="394f1-146">RELATED LINKS</span></span>

[<span data-ttu-id="394f1-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="394f1-147">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="394f1-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="394f1-148">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="394f1-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="394f1-149">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

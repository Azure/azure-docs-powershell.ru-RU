---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F801A78E-6C11-4BD1-BEF4-01C4D6CD36D7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: dcd7b85810c78fa772098f24c428b5f9c8c44183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559503"
---
# <span data-ttu-id="ffff7-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ffff7-101">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="ffff7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ffff7-102">SYNOPSIS</span></span>
<span data-ttu-id="ffff7-103">Включает репликацию для защищенного элемента, создавая защищенный элемент.</span><span class="sxs-lookup"><span data-stu-id="ffff7-103">Enables replication for a protectable item by creating a protected item</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ffff7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ffff7-104">SYNTAX</span></span>

### <span data-ttu-id="ffff7-105">Отключение (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ffff7-105">DisableDR (Default)</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffff7-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="ffff7-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffff7-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="ffff7-107">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffff7-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="ffff7-108">HyperVSiteToAzure</span></span>
```
New-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem> -Name <String>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -RecoveryAzureStorageAccountId <String>
 -OSDiskName <String> -OS <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffff7-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffff7-109">DESCRIPTION</span></span>
<span data-ttu-id="ffff7-110">Командлет **New-AzureRmSiteRecoveryReplicationProtectedItem** создает новый элемент, защищенный репликацией.</span><span class="sxs-lookup"><span data-stu-id="ffff7-110">The **New-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet creates a new Replication Protected item.</span></span>
<span data-ttu-id="ffff7-111">Используйте этот командлет, чтобы включить репликацию для защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="ffff7-111">Use this cmdlet to enable replication for a protectable item.</span></span>

## <span data-ttu-id="ffff7-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ffff7-112">EXAMPLES</span></span>

## <span data-ttu-id="ffff7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ffff7-113">PARAMETERS</span></span>

### <span data-ttu-id="ffff7-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ffff7-114">-Name</span></span>
<span data-ttu-id="ffff7-115">Указывает имя защищенного элемента репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ffff7-115">Specifies the name of the Azure Site Recovery Replication Protected Item.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffff7-116">-OS</span><span class="sxs-lookup"><span data-stu-id="ffff7-116">-OS</span></span>
<span data-ttu-id="ffff7-117">Указывает семейство операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ffff7-117">Specifies the operating system family.</span></span>
<span data-ttu-id="ffff7-118">Допустимые значения этого параметра: Windows или Linux.</span><span class="sxs-lookup"><span data-stu-id="ffff7-118">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffff7-119">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="ffff7-119">-OSDiskName</span></span>
<span data-ttu-id="ffff7-120">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="ffff7-120">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffff7-121">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ffff7-121">-ProtectableItem</span></span>
<span data-ttu-id="ffff7-122">Указывает защищенный элемент Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="ffff7-122">Specifies the Azure Site Recovery Protectable Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffff7-123">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="ffff7-123">-ProtectionContainerMapping</span></span>
<span data-ttu-id="ffff7-124">Указывает объект сопоставления контейнера защиты для Azure Site Recovery, который будет использоваться для репликации.</span><span class="sxs-lookup"><span data-stu-id="ffff7-124">Specifies the Azure Site Recovery Protection Container mapping object to use for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffff7-125">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="ffff7-125">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="ffff7-126">Указывает идентификатор учетной записи хранения Azure, на которую реплицируется этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ffff7-126">Specifies the ID of the Azure storage account that this cmdlet replicates to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffff7-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ffff7-127">-WaitForCompletion</span></span>
<span data-ttu-id="ffff7-128">Указывает, что командлет ожидает завершения.</span><span class="sxs-lookup"><span data-stu-id="ffff7-128">Indicates that the cmdlet waits for completion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffff7-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffff7-129">-Confirm</span></span>
<span data-ttu-id="ffff7-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ffff7-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffff7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffff7-131">-WhatIf</span></span>
<span data-ttu-id="ffff7-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ffff7-132">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ffff7-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ffff7-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffff7-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffff7-134">-DefaultProfile</span></span>
<span data-ttu-id="ffff7-135">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ffff7-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffff7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffff7-136">CommonParameters</span></span>
<span data-ttu-id="ffff7-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ffff7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffff7-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffff7-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffff7-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ffff7-139">INPUTS</span></span>

### <span data-ttu-id="ffff7-140">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ffff7-140">ASRProtectableItem</span></span>
<span data-ttu-id="ffff7-141">Параметр "ProtectableItem" принимает значение типа "ASRProtectableItem" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ffff7-141">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

## <span data-ttu-id="ffff7-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ffff7-142">OUTPUTS</span></span>

### <span data-ttu-id="ffff7-143">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ffff7-143">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ffff7-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ffff7-144">NOTES</span></span>

## <span data-ttu-id="ffff7-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ffff7-145">RELATED LINKS</span></span>

[<span data-ttu-id="ffff7-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ffff7-146">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="ffff7-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ffff7-147">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="ffff7-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ffff7-148">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)

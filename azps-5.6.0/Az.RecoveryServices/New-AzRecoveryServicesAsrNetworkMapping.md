---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: f06635819979823bbbdd298d3873c45ac0a5621a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982307"
---
# <span data-ttu-id="40ca6-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="40ca6-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="40ca6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40ca6-102">SYNOPSIS</span></span>
<span data-ttu-id="40ca6-103">Создается сопоставление сети ASR между двумя сетями.</span><span class="sxs-lookup"><span data-stu-id="40ca6-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="40ca6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="40ca6-104">SYNTAX</span></span>

### <span data-ttu-id="40ca6-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40ca6-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="40ca6-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="40ca6-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40ca6-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="40ca6-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40ca6-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40ca6-108">DESCRIPTION</span></span>
<span data-ttu-id="40ca6-109">Командлет **New-AzRecoveryServicesAsrNetworkMapping** начинает операцию создания сетевого сопоставления ASR между двумя сетями и возвращает объект задания ASR для задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="40ca6-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="40ca6-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="40ca6-110">EXAMPLES</span></span>

### <span data-ttu-id="40ca6-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40ca6-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="40ca6-112">Начало операции создания сопоставления сетей с указанным именем, основными и восстановленными сетями и возврат задания asR для ее отслеживания.</span><span class="sxs-lookup"><span data-stu-id="40ca6-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="40ca6-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="40ca6-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="40ca6-114">Начало сопоставления сети для создания с использованием указанного имени, основных и восстановленных сетей и возврат задания asR для отслеживания операции (сценарий Azure в Azure).</span><span class="sxs-lookup"><span data-stu-id="40ca6-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="40ca6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40ca6-115">PARAMETERS</span></span>

### <span data-ttu-id="40ca6-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="40ca6-116">-AzureToAzure</span></span>
<span data-ttu-id="40ca6-117">Пометить, чтобы создать сценарий AzureToAzure.</span><span class="sxs-lookup"><span data-stu-id="40ca6-117">Flag to create AzureToAzure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ca6-118">-DefaultProfile</span></span>
<span data-ttu-id="40ca6-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40ca6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-120">-Name</span><span class="sxs-lookup"><span data-stu-id="40ca6-120">-Name</span></span>
<span data-ttu-id="40ca6-121">Имя созда создаемого сетевого сопоставления ASR.</span><span class="sxs-lookup"><span data-stu-id="40ca6-121">Name of the ASR network mapping to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="40ca6-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="40ca6-123">Определяет виртуальный сетевой ИД Azure основной сети для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="40ca6-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="40ca6-124">-PrimaryFabric</span></span>
<span data-ttu-id="40ca6-125">Определяет ткань ASR, в которой должно быть создано сопоставление.</span><span class="sxs-lookup"><span data-stu-id="40ca6-125">Specifies the ASR fabric where mapping should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="40ca6-126">-PrimaryNetwork</span></span>
<span data-ttu-id="40ca6-127">Определяет основной объект сети для сопоставления сетей ASR.</span><span class="sxs-lookup"><span data-stu-id="40ca6-127">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="40ca6-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="40ca6-129">Определяет для сопоставления сетей ИД сети Azure для восстановления.</span><span class="sxs-lookup"><span data-stu-id="40ca6-129">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="40ca6-130">-RecoveryFabric</span></span>
<span data-ttu-id="40ca6-131">Объект "Восстановление сайта Azure", соответствующий региону восстановления Azure.</span><span class="sxs-lookup"><span data-stu-id="40ca6-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="40ca6-132">-RecoveryNetwork</span></span>
<span data-ttu-id="40ca6-133">Определяет объект сети восстановления для сопоставления сети ASR.</span><span class="sxs-lookup"><span data-stu-id="40ca6-133">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40ca6-134">-Confirm</span></span>
<span data-ttu-id="40ca6-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40ca6-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40ca6-136">-WhatIf</span></span>
<span data-ttu-id="40ca6-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40ca6-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40ca6-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="40ca6-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40ca6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ca6-139">CommonParameters</span></span>
<span data-ttu-id="40ca6-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40ca6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ca6-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40ca6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ca6-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40ca6-142">INPUTS</span></span>

### <span data-ttu-id="40ca6-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="40ca6-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="40ca6-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="40ca6-144">OUTPUTS</span></span>

### <span data-ttu-id="40ca6-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="40ca6-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="40ca6-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="40ca6-146">NOTES</span></span>

## <span data-ttu-id="40ca6-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40ca6-147">RELATED LINKS</span></span>

[<span data-ttu-id="40ca6-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="40ca6-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="40ca6-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="40ca6-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)

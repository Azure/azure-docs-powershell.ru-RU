---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: b378effc289c1e57505cabfce9dcccffb60f3f52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729669"
---
# <span data-ttu-id="74e5f-101">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="74e5f-101">New-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="74e5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="74e5f-102">SYNOPSIS</span></span>
<span data-ttu-id="74e5f-103">Создание сетевого сопоставления ASR между двумя сетями.</span><span class="sxs-lookup"><span data-stu-id="74e5f-103">Creates an ASR network mapping between two networks.</span></span>

## <span data-ttu-id="74e5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="74e5f-104">SYNTAX</span></span>

### <span data-ttu-id="74e5f-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="74e5f-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="74e5f-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="74e5f-106">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74e5f-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="74e5f-107">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74e5f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="74e5f-108">DESCRIPTION</span></span>
<span data-ttu-id="74e5f-109">Командлет **New-AzRecoveryServicesAsrNetworkMapping** запускает операцию создания сетевого сопоставления ASR из двух сетей и возвращает объект задания ASR для задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="74e5f-109">The **New-AzRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="74e5f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="74e5f-110">EXAMPLES</span></span>

### <span data-ttu-id="74e5f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="74e5f-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="74e5f-112">Запускает операцию создания сетевого сопоставления, используя указанные имя, основную сеть и сети восстановления, и возвращает задание ASR, чтобы отслеживать операцию.</span><span class="sxs-lookup"><span data-stu-id="74e5f-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="74e5f-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="74e5f-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrNetworkMapping -AzToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="74e5f-114">Запускает сетевое сопоставление для создания, используя указанные имя, основную сеть и сети восстановления, и возвращает задание ASR, чтобы отследить операцию (в сценарии Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="74e5f-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="74e5f-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="74e5f-115">PARAMETERS</span></span>

### <span data-ttu-id="74e5f-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="74e5f-116">-AzureToAzure</span></span>
<span data-ttu-id="74e5f-117">{{Fill AzureToAzure Description}}</span><span class="sxs-lookup"><span data-stu-id="74e5f-117">{{Fill AzureToAzure Description}}</span></span>

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

### <span data-ttu-id="74e5f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e5f-118">-DefaultProfile</span></span>
<span data-ttu-id="74e5f-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="74e5f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="74e5f-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="74e5f-120">-Name</span></span>
<span data-ttu-id="74e5f-121">Имя сопоставления сети ASR для создания.</span><span class="sxs-lookup"><span data-stu-id="74e5f-121">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="74e5f-122">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="74e5f-122">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="74e5f-123">Указывает идентификатор виртуальной сети Azure для основной сети для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="74e5f-123">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

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

### <span data-ttu-id="74e5f-124">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="74e5f-124">-PrimaryFabric</span></span>
<span data-ttu-id="74e5f-125">Specifes с помощью ASR Fabric, на котором должно быть создано сопоставление.</span><span class="sxs-lookup"><span data-stu-id="74e5f-125">Specifes the ASR fabric where mapping should be created.</span></span>

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

### <span data-ttu-id="74e5f-126">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="74e5f-126">-PrimaryNetwork</span></span>
<span data-ttu-id="74e5f-127">Задает основной объект сети для сопоставления сети ASR.</span><span class="sxs-lookup"><span data-stu-id="74e5f-127">Specifies the primary network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="74e5f-128">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="74e5f-128">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="74e5f-129">Указывает идентификатор сети Azure Recovery Network для сетевого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="74e5f-129">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="74e5f-130">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="74e5f-130">-RecoveryFabric</span></span>
<span data-ttu-id="74e5f-131">Объект фабрики восстановления сайта Azure, соответствующий региону восстановления Azure.</span><span class="sxs-lookup"><span data-stu-id="74e5f-131">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

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

### <span data-ttu-id="74e5f-132">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="74e5f-132">-RecoveryNetwork</span></span>
<span data-ttu-id="74e5f-133">Указывает сетевой объект для восстановления сетевого сопоставления ASR.</span><span class="sxs-lookup"><span data-stu-id="74e5f-133">Specifies the recovery network object for the ASR network mapping.</span></span>

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

### <span data-ttu-id="74e5f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74e5f-134">-Confirm</span></span>
<span data-ttu-id="74e5f-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="74e5f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74e5f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74e5f-136">-WhatIf</span></span>
<span data-ttu-id="74e5f-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="74e5f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74e5f-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="74e5f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74e5f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e5f-139">CommonParameters</span></span>
<span data-ttu-id="74e5f-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="74e5f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e5f-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74e5f-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e5f-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="74e5f-142">INPUTS</span></span>

### <span data-ttu-id="74e5f-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="74e5f-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="74e5f-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="74e5f-144">OUTPUTS</span></span>

### <span data-ttu-id="74e5f-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="74e5f-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="74e5f-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="74e5f-146">NOTES</span></span>

## <span data-ttu-id="74e5f-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="74e5f-147">RELATED LINKS</span></span>

[<span data-ttu-id="74e5f-148">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="74e5f-148">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="74e5f-149">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="74e5f-149">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)

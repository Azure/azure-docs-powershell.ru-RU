---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: a989b93b2c2ac2a1c292b736275da5cb91c7042d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566150"
---
# <span data-ttu-id="474d5-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="474d5-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="474d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="474d5-102">SYNOPSIS</span></span>
<span data-ttu-id="474d5-103">Создание сетевого сопоставления ASR между двумя сетями.</span><span class="sxs-lookup"><span data-stu-id="474d5-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="474d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="474d5-104">SYNTAX</span></span>

### <span data-ttu-id="474d5-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="474d5-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="474d5-106">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="474d5-106">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping [-AzureToAzure] -Name <String> -PrimaryFabric <ASRFabric>
 -PrimaryAzureNetworkId <String> -RecoveryFabric <ASRFabric> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="474d5-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="474d5-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="474d5-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="474d5-108">DESCRIPTION</span></span>
<span data-ttu-id="474d5-109">Командлет **New-AzureRmRecoveryServicesAsrNetworkMapping** запускает операцию создания сетевого сопоставления ASR из двух сетей и возвращает объект задания ASR для задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="474d5-109">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="474d5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="474d5-110">EXAMPLES</span></span>

### <span data-ttu-id="474d5-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="474d5-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="474d5-112">Запускает операцию создания сетевого сопоставления, используя указанные имя, основную сеть и сети восстановления, и возвращает задание ASR, чтобы отслеживать операцию.</span><span class="sxs-lookup"><span data-stu-id="474d5-112">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

### <span data-ttu-id="474d5-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="474d5-113">Example 2</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -AzureToAzure -Name "mappingName" -PrimaryFabric $AzureFabric `
 -PrimaryAzureNetworkId $AzureNetworkId -RecoveryFabric $RecoveryAzureFabric -RecoveryAzureNetworkId $RecoveryNetworkId
```

<span data-ttu-id="474d5-114">Запускает сетевое сопоставление для создания, используя указанные имя, основную сеть и сети восстановления, и возвращает задание ASR, чтобы отследить операцию (в сценарии Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="474d5-114">Starts the network mapping for creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation(Azure to Azure scenario).</span></span>

## <span data-ttu-id="474d5-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="474d5-115">PARAMETERS</span></span>

### <span data-ttu-id="474d5-116">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="474d5-116">-AzureToAzure</span></span>
<span data-ttu-id="474d5-117">Параметр Switch, указывающий, что создаваемое Сетевое сопоставление будет использоваться для репликации виртуальных машин Azure между двумя областями Azure.</span><span class="sxs-lookup"><span data-stu-id="474d5-117">Switch parameter specifying that the network mapping being created will be used to replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="474d5-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="474d5-118">-Confirm</span></span>
<span data-ttu-id="474d5-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="474d5-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="474d5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="474d5-120">-DefaultProfile</span></span>
<span data-ttu-id="474d5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="474d5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="474d5-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="474d5-122">-Name</span></span>
<span data-ttu-id="474d5-123">Имя сопоставления сети ASR для создания.</span><span class="sxs-lookup"><span data-stu-id="474d5-123">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="474d5-124">-PrimaryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="474d5-124">-PrimaryAzureNetworkId</span></span>
<span data-ttu-id="474d5-125">Указывает идентификатор виртуальной сети Azure для основной сети для сопоставления.</span><span class="sxs-lookup"><span data-stu-id="474d5-125">Specifies the Azure virtual network ID of the primary network for the mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="474d5-126">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="474d5-126">-PrimaryFabric</span></span>
<span data-ttu-id="474d5-127">Specifes с помощью ASR Fabric, на котором должно быть создано сопоставление.</span><span class="sxs-lookup"><span data-stu-id="474d5-127">Specifes the ASR fabric where mapping should be created.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="474d5-128">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="474d5-128">-PrimaryNetwork</span></span>
<span data-ttu-id="474d5-129">Задает основной объект сети для сопоставления сети ASR.</span><span class="sxs-lookup"><span data-stu-id="474d5-129">Specifies the primary network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="474d5-130">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="474d5-130">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="474d5-131">Указывает идентификатор сети Azure Recovery Network для сетевого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="474d5-131">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, EnterpriseToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="474d5-132">-RecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="474d5-132">-RecoveryFabric</span></span>
<span data-ttu-id="474d5-133">Объект фабрики восстановления сайта Azure, соответствующий региону восстановления Azure.</span><span class="sxs-lookup"><span data-stu-id="474d5-133">The Azure Site Recovery fabric object corresponding to the recovery Azure region.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="474d5-134">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="474d5-134">-RecoveryNetwork</span></span>
<span data-ttu-id="474d5-135">Указывает сетевой объект для восстановления сетевого сопоставления ASR.</span><span class="sxs-lookup"><span data-stu-id="474d5-135">Specifies the recovery network object for the ASR network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="474d5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="474d5-136">-WhatIf</span></span>
<span data-ttu-id="474d5-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="474d5-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="474d5-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="474d5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="474d5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="474d5-139">CommonParameters</span></span>
<span data-ttu-id="474d5-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="474d5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="474d5-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="474d5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="474d5-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="474d5-142">INPUTS</span></span>

### <span data-ttu-id="474d5-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="474d5-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="474d5-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="474d5-144">OUTPUTS</span></span>

### <span data-ttu-id="474d5-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="474d5-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="474d5-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="474d5-146">NOTES</span></span>

## <span data-ttu-id="474d5-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="474d5-147">RELATED LINKS</span></span>

[<span data-ttu-id="474d5-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="474d5-148">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="474d5-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="474d5-149">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)

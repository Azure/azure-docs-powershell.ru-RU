---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 1da06582d442c96f74579e9fdf3009325f996012
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734319"
---
# <span data-ttu-id="49696-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="49696-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="49696-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49696-102">SYNOPSIS</span></span>
<span data-ttu-id="49696-103">Создает структуру восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="49696-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49696-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49696-104">SYNTAX</span></span>

### <span data-ttu-id="49696-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49696-105">Default (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49696-106">Служба</span><span class="sxs-lookup"><span data-stu-id="49696-106">Azure</span></span>
```
New-AzureRmRecoveryServicesAsrFabric [-Azure] -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49696-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49696-107">DESCRIPTION</span></span>
<span data-ttu-id="49696-108">Командлет **New-AzureRmRecoveryServicesAsrFabric** создает структуру восстановления сайта Azure для указанного типа.</span><span class="sxs-lookup"><span data-stu-id="49696-108">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="49696-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49696-109">EXAMPLES</span></span>

### <span data-ttu-id="49696-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49696-110">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="49696-111">Запускает создание структуры с передаваемым именем и возвращает задание ASR, используемое для отслеживания операции создания структуры.</span><span class="sxs-lookup"><span data-stu-id="49696-111">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

### <span data-ttu-id="49696-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="49696-112">Example 2</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Azure -Name $fabricName -Location "eastus"
PS C:\>  Get-ASRJob -name $currentJob.id
```

<span data-ttu-id="49696-113">Запускает создание структуры Azure с передаваемым именем и возвращает задание ASR, используемое для отслеживания операции создания структуры.</span><span class="sxs-lookup"><span data-stu-id="49696-113">Starts the azure fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="49696-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49696-114">PARAMETERS</span></span>

### <span data-ttu-id="49696-115">-Azure</span><span class="sxs-lookup"><span data-stu-id="49696-115">-Azure</span></span>
<span data-ttu-id="49696-116">Параметр Switch указывает на создание Azure Fabric.</span><span class="sxs-lookup"><span data-stu-id="49696-116">Switch parameter indicates creation of azure fabric.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49696-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49696-117">-DefaultProfile</span></span>
<span data-ttu-id="49696-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49696-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="49696-119">-Location</span><span class="sxs-lookup"><span data-stu-id="49696-119">-Location</span></span>
<span data-ttu-id="49696-120">Указывает область Azure, соответствующую создаваемому объекту фабрики.</span><span class="sxs-lookup"><span data-stu-id="49696-120">Specifies the Azure region corresponding to the Fabric object being created.</span></span> <span data-ttu-id="49696-121">Объект фабрики восстановления сайта Azure представляет регион.</span><span class="sxs-lookup"><span data-stu-id="49696-121">The Azure Site Recovery fabric object represents a region.</span></span> <span data-ttu-id="49696-122">Для виртуальных машин, реплицируемых между двумя областями Azure, основная структура представляет первичный регион Azure и структуру восстановления.</span><span class="sxs-lookup"><span data-stu-id="49696-122">For virtual machines being replicated between two Azure regions  a primary fabric represents the primary Azure region and the recovery fabric .</span></span>

```yaml
Type: System.String
Parameter Sets: Azure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49696-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49696-123">-Name</span></span>
<span data-ttu-id="49696-124">Указывает имя структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="49696-124">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="49696-125">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="49696-125">-Type</span></span>
<span data-ttu-id="49696-126">Указывает тип структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="49696-126">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49696-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49696-127">-Confirm</span></span>
<span data-ttu-id="49696-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49696-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49696-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49696-129">-WhatIf</span></span>
<span data-ttu-id="49696-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49696-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49696-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49696-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49696-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49696-132">CommonParameters</span></span>
<span data-ttu-id="49696-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49696-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49696-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49696-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49696-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49696-135">INPUTS</span></span>

### <span data-ttu-id="49696-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="49696-136">None</span></span>

## <span data-ttu-id="49696-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49696-137">OUTPUTS</span></span>

### <span data-ttu-id="49696-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="49696-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="49696-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="49696-139">NOTES</span></span>

## <span data-ttu-id="49696-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49696-140">RELATED LINKS</span></span>

[<span data-ttu-id="49696-141">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="49696-141">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="49696-142">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="49696-142">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)

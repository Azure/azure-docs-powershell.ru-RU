---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: 28c038a6dfd29f9daaeb942afa8fcb4c479cd0aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734526"
---
# <span data-ttu-id="54fa9-101">New-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="54fa9-101">New-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="54fa9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="54fa9-103">Создает структуру восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="54fa9-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54fa9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54fa9-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrFabric -Name <String> [-Type <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54fa9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54fa9-105">DESCRIPTION</span></span>
<span data-ttu-id="54fa9-106">Командлет **New-AzureRmRecoveryServicesAsrFabric** создает структуру восстановления сайта Azure для указанного типа.</span><span class="sxs-lookup"><span data-stu-id="54fa9-106">The **New-AzureRmRecoveryServicesAsrFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="54fa9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54fa9-107">EXAMPLES</span></span>

### <span data-ttu-id="54fa9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54fa9-108">Example 1</span></span>
```
PS C:\>  $currentJob = New-AzureRmRecoveryServicesAsrFabric -Name $FabricName
```

<span data-ttu-id="54fa9-109">Запускает создание структуры с передаваемым именем и возвращает задание ASR, используемое для отслеживания операции создания структуры.</span><span class="sxs-lookup"><span data-stu-id="54fa9-109">Starts the fabric creation with passed name and returns the ASR job used to track the fabric creation operation.</span></span>

## <span data-ttu-id="54fa9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54fa9-110">PARAMETERS</span></span>

### <span data-ttu-id="54fa9-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54fa9-111">-Name</span></span>
<span data-ttu-id="54fa9-112">Указывает имя структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="54fa9-112">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="54fa9-113">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="54fa9-113">-Type</span></span>
<span data-ttu-id="54fa9-114">Указывает тип структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="54fa9-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54fa9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54fa9-115">-Confirm</span></span>
<span data-ttu-id="54fa9-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54fa9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54fa9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fa9-117">-WhatIf</span></span>
<span data-ttu-id="54fa9-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54fa9-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54fa9-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54fa9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54fa9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fa9-120">CommonParameters</span></span>
<span data-ttu-id="54fa9-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54fa9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fa9-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54fa9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fa9-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54fa9-123">INPUTS</span></span>

### <span data-ttu-id="54fa9-124">Ничего</span><span class="sxs-lookup"><span data-stu-id="54fa9-124">None</span></span>

## <span data-ttu-id="54fa9-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54fa9-125">OUTPUTS</span></span>

### <span data-ttu-id="54fa9-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="54fa9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="54fa9-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="54fa9-127">NOTES</span></span>

## <span data-ttu-id="54fa9-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54fa9-128">RELATED LINKS</span></span>

[<span data-ttu-id="54fa9-129">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="54fa9-129">Get-AzureRmRecoveryServicesAsrFabric</span></span>](./Get-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="54fa9-130">Remove-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="54fa9-130">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)

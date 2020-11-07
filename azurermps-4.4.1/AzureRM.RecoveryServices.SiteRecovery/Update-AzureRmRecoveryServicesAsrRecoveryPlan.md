---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 21a46346c681a6f184033d4f50d65e6c9a019844
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733643"
---
# <span data-ttu-id="35caa-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="35caa-101">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="35caa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35caa-102">SYNOPSIS</span></span>
<span data-ttu-id="35caa-103">Обновляет содержимое плана восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="35caa-103">Updates the contents of an Azure Site recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35caa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35caa-104">SYNTAX</span></span>

### <span data-ttu-id="35caa-105">ByRPObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35caa-105">ByRPObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35caa-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="35caa-106">ByRPFile</span></span>
```
Update-AzureRmRecoveryServicesAsrRecoveryPlan -Path <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35caa-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35caa-107">DESCRIPTION</span></span>
<span data-ttu-id="35caa-108">Командлет **Update-AzureRmRecoveryServicesAsrRecoveryPlan** обновляет содержимое плана восстановления с помощью содержимого указанного объекта плана восстановления ASR или JSON-файла определения плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="35caa-108">The **Update-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="35caa-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35caa-109">EXAMPLES</span></span>

### <span data-ttu-id="35caa-110">Пример 1: Обновление плана восстановления</span><span class="sxs-lookup"><span data-stu-id="35caa-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="35caa-111">Запуск операции обновления плана восстановления с помощью содержимого указанного объекта плана восстановления ASR и возврат задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="35caa-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="35caa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35caa-112">PARAMETERS</span></span>

### <span data-ttu-id="35caa-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35caa-113">-InputObject</span></span>
<span data-ttu-id="35caa-114">Входной объект для командлета: определяет объект плана восстановления ASR, содержимое которого используется для обновления плана восстановления, на который ссылается объект.</span><span class="sxs-lookup"><span data-stu-id="35caa-114">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35caa-115">-Path</span><span class="sxs-lookup"><span data-stu-id="35caa-115">-Path</span></span>
<span data-ttu-id="35caa-116">Указывает путь JSON файла определения плана восстановления, используемого для обновления плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="35caa-116">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: String
Parameter Sets: ByRPFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35caa-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35caa-117">-Confirm</span></span>
<span data-ttu-id="35caa-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35caa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35caa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35caa-119">-WhatIf</span></span>
<span data-ttu-id="35caa-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35caa-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35caa-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35caa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35caa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35caa-122">CommonParameters</span></span>
<span data-ttu-id="35caa-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35caa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35caa-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35caa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35caa-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35caa-125">INPUTS</span></span>

### <span data-ttu-id="35caa-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="35caa-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="35caa-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35caa-127">OUTPUTS</span></span>

### <span data-ttu-id="35caa-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="35caa-128">System.Object</span></span>

## <span data-ttu-id="35caa-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="35caa-129">NOTES</span></span>

## <span data-ttu-id="35caa-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35caa-130">RELATED LINKS</span></span>

[<span data-ttu-id="35caa-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="35caa-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="35caa-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="35caa-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="35caa-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="35caa-133">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md)



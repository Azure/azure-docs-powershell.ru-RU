---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 99c91f24bcc81ee6d6971b74779dfd116b90fdef
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073512"
---
# <span data-ttu-id="0a193-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0a193-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="0a193-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a193-102">SYNOPSIS</span></span>
<span data-ttu-id="0a193-103">Обновляет содержимое плана восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="0a193-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="0a193-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a193-104">SYNTAX</span></span>

### <span data-ttu-id="0a193-105">ByRPObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a193-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a193-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="0a193-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a193-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a193-107">DESCRIPTION</span></span>
<span data-ttu-id="0a193-108">Командлет **Update-AzRecoveryServicesAsrRecoveryPlan** обновляет содержимое плана восстановления с помощью содержимого указанного объекта плана восстановления ASR или JSON-файла определения плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="0a193-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="0a193-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a193-109">EXAMPLES</span></span>

### <span data-ttu-id="0a193-110">Пример 1: Обновление плана восстановления</span><span class="sxs-lookup"><span data-stu-id="0a193-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="0a193-111">Запуск операции обновления плана восстановления с помощью содержимого указанного объекта плана восстановления ASR и возврат задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="0a193-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="0a193-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a193-112">PARAMETERS</span></span>

### <span data-ttu-id="0a193-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a193-113">-DefaultProfile</span></span>
<span data-ttu-id="0a193-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a193-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="0a193-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a193-115">-InputObject</span></span>
<span data-ttu-id="0a193-116">Входной объект для командлета: определяет объект плана восстановления ASR, содержимое которого используется для обновления плана восстановления, на который ссылается объект.</span><span class="sxs-lookup"><span data-stu-id="0a193-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a193-117">-Path</span><span class="sxs-lookup"><span data-stu-id="0a193-117">-Path</span></span>
<span data-ttu-id="0a193-118">Указывает путь JSON файла определения плана восстановления, используемого для обновления плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="0a193-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a193-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a193-119">-Confirm</span></span>
<span data-ttu-id="0a193-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a193-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a193-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a193-121">-WhatIf</span></span>
<span data-ttu-id="0a193-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a193-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a193-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a193-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a193-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a193-124">CommonParameters</span></span>
<span data-ttu-id="0a193-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a193-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a193-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a193-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a193-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a193-127">INPUTS</span></span>

### <span data-ttu-id="0a193-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0a193-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="0a193-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a193-129">OUTPUTS</span></span>

### <span data-ttu-id="0a193-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="0a193-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="0a193-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a193-131">NOTES</span></span>

## <span data-ttu-id="0a193-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a193-132">RELATED LINKS</span></span>

[<span data-ttu-id="0a193-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0a193-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="0a193-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0a193-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="0a193-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="0a193-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 99c91f24bcc81ee6d6971b74779dfd116b90fdef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413492"
---
# <span data-ttu-id="20f5d-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="20f5d-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="20f5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="20f5d-103">Обновляет содержимое плана восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="20f5d-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="20f5d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="20f5d-104">SYNTAX</span></span>

### <span data-ttu-id="20f5d-105">ByRPObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20f5d-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20f5d-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="20f5d-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20f5d-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20f5d-107">DESCRIPTION</span></span>
<span data-ttu-id="20f5d-108">С помощью **cmdlet Update-AzRecoveryServicesAsrRecoveryPlan** содержимое плана восстановления обновляется с использованием содержимого указанного объекта плана восстановления ASR или JSON-файла определения плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="20f5d-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="20f5d-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="20f5d-109">EXAMPLES</span></span>

### <span data-ttu-id="20f5d-110">Пример 1. Обновление плана восстановления</span><span class="sxs-lookup"><span data-stu-id="20f5d-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="20f5d-111">Начните операцию обновления плана восстановления с использованием содержимого указанного объекта плана восстановления ASR и возвращает задание asR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="20f5d-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="20f5d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20f5d-112">PARAMETERS</span></span>

### <span data-ttu-id="20f5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f5d-113">-DefaultProfile</span></span>
<span data-ttu-id="20f5d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20f5d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="20f5d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20f5d-115">-InputObject</span></span>
<span data-ttu-id="20f5d-116">Объект ввода для cmdlet: определяет объект плана восстановления ASR, содержимое которого используется для обновления плана восстановления, на который ссылается этот объект.</span><span class="sxs-lookup"><span data-stu-id="20f5d-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

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

### <span data-ttu-id="20f5d-117">-Path</span><span class="sxs-lookup"><span data-stu-id="20f5d-117">-Path</span></span>
<span data-ttu-id="20f5d-118">Путь к JSON-файлу определения плана восстановления, который использовался для обновления плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="20f5d-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

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

### <span data-ttu-id="20f5d-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20f5d-119">-Confirm</span></span>
<span data-ttu-id="20f5d-120">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="20f5d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20f5d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20f5d-121">-WhatIf</span></span>
<span data-ttu-id="20f5d-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20f5d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20f5d-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="20f5d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20f5d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f5d-124">CommonParameters</span></span>
<span data-ttu-id="20f5d-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f5d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f5d-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20f5d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f5d-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20f5d-127">INPUTS</span></span>

### <span data-ttu-id="20f5d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="20f5d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="20f5d-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="20f5d-129">OUTPUTS</span></span>

### <span data-ttu-id="20f5d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="20f5d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="20f5d-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="20f5d-131">NOTES</span></span>

## <span data-ttu-id="20f5d-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20f5d-132">RELATED LINKS</span></span>

[<span data-ttu-id="20f5d-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="20f5d-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="20f5d-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="20f5d-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="20f5d-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="20f5d-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)

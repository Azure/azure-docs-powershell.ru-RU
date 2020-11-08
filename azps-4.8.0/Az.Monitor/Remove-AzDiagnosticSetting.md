---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdiagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDiagnosticSetting.md
ms.openlocfilehash: f165396d5b3af823d91e7c06d2f1cb93eb2eaafd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078980"
---
# <span data-ttu-id="4072d-101">Remove-AzDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="4072d-101">Remove-AzDiagnosticSetting</span></span>

## <span data-ttu-id="4072d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4072d-102">SYNOPSIS</span></span>
<span data-ttu-id="4072d-103">Удаление диагностического параметра для ресурса.</span><span class="sxs-lookup"><span data-stu-id="4072d-103">Remove a diagnostic setting for the a resource.</span></span>

## <span data-ttu-id="4072d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4072d-104">SYNTAX</span></span>

```
Remove-AzDiagnosticSetting -ResourceId <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4072d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4072d-105">DESCRIPTION</span></span>
<span data-ttu-id="4072d-106">Командлет **Remove-AzDiagnosticSetting** удаляет параметр диагностики для определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="4072d-106">The **Remove-AzDiagnosticSetting** cmdlet removes the diagnostic setting for the particular resource.</span></span>
<span data-ttu-id="4072d-107">Этот командлет реализует шаблон ShouldProcess, т. е. может запросить подтверждение от пользователя, прежде чем действительно создать, изменить или удалить ресурс.</span><span class="sxs-lookup"><span data-stu-id="4072d-107">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="4072d-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4072d-108">EXAMPLES</span></span>

### <span data-ttu-id="4072d-109">Пример 1: Удаление параметра диагностики по умолчанию (службы) для ресурса</span><span class="sxs-lookup"><span data-stu-id="4072d-109">Example 1: Remove the default diagnostic setting (service) for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01"
```

<span data-ttu-id="4072d-110">Эта команда удаляет параметр диагностики по умолчанию (службу) для ресурса с именем Resource01.</span><span class="sxs-lookup"><span data-stu-id="4072d-110">This command removes the default diagnostic setting (service) for the resource called Resource01.</span></span>

### <span data-ttu-id="4072d-111">Пример 2: Удаление параметра диагностики по умолчанию, определяемого указанным именем для ресурса</span><span class="sxs-lookup"><span data-stu-id="4072d-111">Example 2: Remove the default diagnostic setting identified by the given name for a resource</span></span>
```
PS C:\>Remove-AzDiagnosticSetting -ResourceId "Resource01" -Name myDiagSetting
```

<span data-ttu-id="4072d-112">Эта команда удаляет параметр диагностики, именуемый myDiagSetting, для ресурса с именем Resource01.</span><span class="sxs-lookup"><span data-stu-id="4072d-112">This command removes the diagnostic setting called myDiagSetting for the resource called Resource01.</span></span>

## <span data-ttu-id="4072d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4072d-113">PARAMETERS</span></span>

### <span data-ttu-id="4072d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4072d-114">-DefaultProfile</span></span>
<span data-ttu-id="4072d-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4072d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4072d-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4072d-116">-Name</span></span>
<span data-ttu-id="4072d-117">Имя параметра диагностики.</span><span class="sxs-lookup"><span data-stu-id="4072d-117">The name of the diagnostic setting.</span></span> <span data-ttu-id="4072d-118">Если не задано значение по умолчанию "Service" для звонка, так как оно находится в предыдущем API, и этот командлет отключит только все категории для метрики и журналов.</span><span class="sxs-lookup"><span data-stu-id="4072d-118">If not given the call default to "service" as it was in the previous API and this cmdlet will only disable all categories for metrics/logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4072d-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4072d-119">-ResourceId</span></span>
<span data-ttu-id="4072d-120">Указывает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4072d-120">Specifies the ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4072d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4072d-121">-Confirm</span></span>
<span data-ttu-id="4072d-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4072d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4072d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4072d-123">-WhatIf</span></span>
<span data-ttu-id="4072d-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4072d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4072d-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4072d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4072d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4072d-126">CommonParameters</span></span>
<span data-ttu-id="4072d-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4072d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4072d-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4072d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4072d-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4072d-129">INPUTS</span></span>

### <span data-ttu-id="4072d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4072d-130">System.String</span></span>

## <span data-ttu-id="4072d-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4072d-131">OUTPUTS</span></span>

### <span data-ttu-id="4072d-132">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="4072d-132">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="4072d-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="4072d-133">NOTES</span></span>

## <span data-ttu-id="4072d-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4072d-134">RELATED LINKS</span></span>

<span data-ttu-id="4072d-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md) 
 [Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span><span class="sxs-lookup"><span data-stu-id="4072d-135">[Get-AzDiagnosticSetting](./Get-AzDiagnosticSetting.md)
[Set-AzDiagnosticSetting](./Set-AzDiagnosticSetting.md)</span></span>

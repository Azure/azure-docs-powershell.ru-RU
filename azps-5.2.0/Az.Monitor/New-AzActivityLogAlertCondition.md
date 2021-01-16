---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 85cf08b0ade67042c4aa4c4c5ff3253b6af9f2ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396567"
---
# <span data-ttu-id="446a1-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="446a1-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="446a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="446a1-102">SYNOPSIS</span></span>
<span data-ttu-id="446a1-103">Создание объекта условия оповещения журнала действий в памяти.</span><span class="sxs-lookup"><span data-stu-id="446a1-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="446a1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="446a1-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="446a1-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="446a1-105">DESCRIPTION</span></span>
<span data-ttu-id="446a1-106">С **его учетом** в памяти создается новый объект условий оповещений журнала действий.</span><span class="sxs-lookup"><span data-stu-id="446a1-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="446a1-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="446a1-107">EXAMPLES</span></span>

### <span data-ttu-id="446a1-108">Пример 1. Создание объекта условия оповещения журнала действий в памяти.</span><span class="sxs-lookup"><span data-stu-id="446a1-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="446a1-109">Эта команда создает новый объект условия оповещения журнала действий в памяти.</span><span class="sxs-lookup"><span data-stu-id="446a1-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="446a1-110">**ПРИМЕЧАНИЕ.** Если этот cmdlet используется с [Set-AzActivityLogAlert](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert) по крайней мере одного из этих объектов, переданных в качестве параметров, его поле должно иметь "Category".</span><span class="sxs-lookup"><span data-stu-id="446a1-110">**NOTE**: when this cmdlet is used with [Set-AzActivityLogAlert](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert) at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="446a1-111">В противном случае на задний счет отвечает 400 (BadRequest).)</span><span class="sxs-lookup"><span data-stu-id="446a1-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="446a1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="446a1-112">PARAMETERS</span></span>

### <span data-ttu-id="446a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="446a1-113">-DefaultProfile</span></span>
<span data-ttu-id="446a1-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="446a1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="446a1-115">-Equal</span><span class="sxs-lookup"><span data-stu-id="446a1-115">-Equal</span></span>
<span data-ttu-id="446a1-116">Определяет свойство "Равно" для условия "лист".</span><span class="sxs-lookup"><span data-stu-id="446a1-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="446a1-117">-Поле</span><span class="sxs-lookup"><span data-stu-id="446a1-117">-Field</span></span>
<span data-ttu-id="446a1-118">Определяет поле условия.</span><span class="sxs-lookup"><span data-stu-id="446a1-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="446a1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="446a1-119">CommonParameters</span></span>
<span data-ttu-id="446a1-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="446a1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="446a1-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="446a1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="446a1-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="446a1-122">INPUTS</span></span>

### <span data-ttu-id="446a1-123">System.String</span><span class="sxs-lookup"><span data-stu-id="446a1-123">System.String</span></span>

## <span data-ttu-id="446a1-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="446a1-124">OUTPUTS</span></span>

### <span data-ttu-id="446a1-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="446a1-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="446a1-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="446a1-126">NOTES</span></span>

## <span data-ttu-id="446a1-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="446a1-127">RELATED LINKS</span></span>

[<span data-ttu-id="446a1-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="446a1-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="446a1-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="446a1-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="446a1-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="446a1-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="446a1-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="446a1-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="446a1-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="446a1-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="446a1-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="446a1-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
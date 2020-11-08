---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 4932445406e19cbc05f5e2680871a03ae6f40f60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078186"
---
# <span data-ttu-id="2471d-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="2471d-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="2471d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2471d-102">SYNOPSIS</span></span>
<span data-ttu-id="2471d-103">Создает новый объект условия предупреждения журнала активности в памяти.</span><span class="sxs-lookup"><span data-stu-id="2471d-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="2471d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2471d-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2471d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2471d-105">DESCRIPTION</span></span>
<span data-ttu-id="2471d-106">Командлет **New-AzActivityLogAlertCondition** создает новый объект условия оповещения журнала активности в памяти.</span><span class="sxs-lookup"><span data-stu-id="2471d-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="2471d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2471d-107">EXAMPLES</span></span>

### <span data-ttu-id="2471d-108">Пример 1: создание в памяти нового объекта условия для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="2471d-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="2471d-109">Эта команда создает новый объект условия оповещения журнала активности в памяти.</span><span class="sxs-lookup"><span data-stu-id="2471d-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="2471d-110">**Примечание**. Если этот командлет используется с Set-AzActivityLogAlert хотя бы один из этих объектов, переданный как параметры, то его поле должно быть равно "Category".</span><span class="sxs-lookup"><span data-stu-id="2471d-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="2471d-111">В противном случае серверный элемент реагирует на 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="2471d-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="2471d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2471d-112">PARAMETERS</span></span>

### <span data-ttu-id="2471d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2471d-113">-DefaultProfile</span></span>
<span data-ttu-id="2471d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2471d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2471d-115">-Равно</span><span class="sxs-lookup"><span data-stu-id="2471d-115">-Equal</span></span>
<span data-ttu-id="2471d-116">Указывает свойство Equals конечного условия.</span><span class="sxs-lookup"><span data-stu-id="2471d-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="2471d-117">-Field</span><span class="sxs-lookup"><span data-stu-id="2471d-117">-Field</span></span>
<span data-ttu-id="2471d-118">Определяет поле для условия.</span><span class="sxs-lookup"><span data-stu-id="2471d-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="2471d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2471d-119">CommonParameters</span></span>
<span data-ttu-id="2471d-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2471d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2471d-121">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2471d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2471d-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2471d-122">INPUTS</span></span>

### <span data-ttu-id="2471d-123">System. String</span><span class="sxs-lookup"><span data-stu-id="2471d-123">System.String</span></span>

## <span data-ttu-id="2471d-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2471d-124">OUTPUTS</span></span>

### <span data-ttu-id="2471d-125">Microsoft. Azure. Management. Monitor. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="2471d-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="2471d-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="2471d-126">NOTES</span></span>

## <span data-ttu-id="2471d-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2471d-127">RELATED LINKS</span></span>

[<span data-ttu-id="2471d-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2471d-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="2471d-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2471d-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="2471d-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2471d-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="2471d-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2471d-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="2471d-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2471d-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="2471d-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="2471d-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: 3904be513baf73c67c2dbd0018ae6b3e7e2226fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564447"
---
# <span data-ttu-id="9f864-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="9f864-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="9f864-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f864-102">SYNOPSIS</span></span>
<span data-ttu-id="9f864-103">Создает новый объект условия предупреждения журнала активности в памяти.</span><span class="sxs-lookup"><span data-stu-id="9f864-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f864-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f864-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f864-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f864-105">DESCRIPTION</span></span>
<span data-ttu-id="9f864-106">Командлет **New-AzureRmActivityLogAlertCondition** создает новый объект условия оповещения журнала активности в памяти.</span><span class="sxs-lookup"><span data-stu-id="9f864-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="9f864-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f864-107">EXAMPLES</span></span>

### <span data-ttu-id="9f864-108">Пример 1: создание в памяти нового объекта условия для оповещения журнала активности.</span><span class="sxs-lookup"><span data-stu-id="9f864-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="9f864-109">Эта команда создает новый объект условия оповещения журнала активности в памяти.</span><span class="sxs-lookup"><span data-stu-id="9f864-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="9f864-110">**Примечание**. Если этот командлет используется с Set-AzureRmActivityLogAlert хотя бы один из этих объектов, переданный как параметры, то его поле должно быть равно "Category".</span><span class="sxs-lookup"><span data-stu-id="9f864-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="9f864-111">В противном случае серверный элемент реагирует на 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="9f864-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="9f864-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f864-112">PARAMETERS</span></span>

### <span data-ttu-id="9f864-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f864-113">-DefaultProfile</span></span>
<span data-ttu-id="9f864-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9f864-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f864-115">-Равно</span><span class="sxs-lookup"><span data-stu-id="9f864-115">-Equal</span></span>
<span data-ttu-id="9f864-116">Указывает свойство Equals конечного условия.</span><span class="sxs-lookup"><span data-stu-id="9f864-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="9f864-117">-Field</span><span class="sxs-lookup"><span data-stu-id="9f864-117">-Field</span></span>
<span data-ttu-id="9f864-118">Определяет поле для условия.</span><span class="sxs-lookup"><span data-stu-id="9f864-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="9f864-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f864-119">CommonParameters</span></span>
<span data-ttu-id="9f864-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f864-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f864-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f864-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f864-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f864-122">INPUTS</span></span>

### <span data-ttu-id="9f864-123">System. String</span><span class="sxs-lookup"><span data-stu-id="9f864-123">System.String</span></span>

## <span data-ttu-id="9f864-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f864-124">OUTPUTS</span></span>

### <span data-ttu-id="9f864-125">Microsoft. Azure. Management. Monitor. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="9f864-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="9f864-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f864-126">NOTES</span></span>

## <span data-ttu-id="9f864-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f864-127">RELATED LINKS</span></span>

[<span data-ttu-id="9f864-128">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9f864-128">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9f864-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9f864-129">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9f864-130">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9f864-130">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9f864-131">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9f864-131">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9f864-132">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9f864-132">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9f864-133">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="9f864-133">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)

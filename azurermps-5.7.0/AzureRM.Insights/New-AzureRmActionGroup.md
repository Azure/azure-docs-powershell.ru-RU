---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: 9428ea3c297bcdab01ee6464d38b5c20910b69d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732644"
---
# <span data-ttu-id="25364-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="25364-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="25364-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="25364-102">SYNOPSIS</span></span>
<span data-ttu-id="25364-103">Создает объект ссылки на ActionGroup в памяти.</span><span class="sxs-lookup"><span data-stu-id="25364-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25364-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="25364-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25364-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25364-105">DESCRIPTION</span></span>
<span data-ttu-id="25364-106">Командлет **New-AzureRmActionGroup** создает объект ссылки на группу действий в памяти.</span><span class="sxs-lookup"><span data-stu-id="25364-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="25364-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="25364-107">EXAMPLES</span></span>

### <span data-ttu-id="25364-108">Пример 1: создание объекта ссылки на группу действий в памяти</span><span class="sxs-lookup"><span data-stu-id="25364-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="25364-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="25364-109">PARAMETERS</span></span>

### <span data-ttu-id="25364-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="25364-110">-ActionGroupId</span></span>
<span data-ttu-id="25364-111">Идентификатор или имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="25364-111">The Id/name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25364-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25364-112">-DefaultProfile</span></span>
<span data-ttu-id="25364-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="25364-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25364-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="25364-114">-WebhookProperty</span></span>
<span data-ttu-id="25364-115">Свойства веб-перехватчика группы "действия"</span><span class="sxs-lookup"><span data-stu-id="25364-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25364-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25364-116">CommonParameters</span></span>
<span data-ttu-id="25364-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="25364-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25364-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25364-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25364-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="25364-119">INPUTS</span></span>

### <span data-ttu-id="25364-120">Ничего</span><span class="sxs-lookup"><span data-stu-id="25364-120">None</span></span>
<span data-ttu-id="25364-121">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="25364-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="25364-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="25364-122">OUTPUTS</span></span>

### <span data-ttu-id="25364-123">Microsoft. Azure. Management. Monitor. Management. Models. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="25364-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="25364-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="25364-124">NOTES</span></span>

## <span data-ttu-id="25364-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25364-125">RELATED LINKS</span></span>

[<span data-ttu-id="25364-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25364-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="25364-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25364-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="25364-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25364-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="25364-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25364-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="25364-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="25364-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="25364-131">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="25364-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)


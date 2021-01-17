---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroup.md
ms.openlocfilehash: 99fb63a5dd4ba60b44e96139418a76701334444e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98411663"
---
# <span data-ttu-id="41f00-101">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="41f00-101">New-AzActionGroup</span></span>

## <span data-ttu-id="41f00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41f00-102">SYNOPSIS</span></span>
<span data-ttu-id="41f00-103">Создание объекта-ссылки ActionGroup в памяти.</span><span class="sxs-lookup"><span data-stu-id="41f00-103">Creates an ActionGroup reference object in memory.</span></span>

## <span data-ttu-id="41f00-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="41f00-104">SYNTAX</span></span>

```
New-AzActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41f00-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41f00-105">DESCRIPTION</span></span>
<span data-ttu-id="41f00-106">Для **этого в памяти создается** объект ссылки на группу действий.</span><span class="sxs-lookup"><span data-stu-id="41f00-106">The **New-AzActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="41f00-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="41f00-107">EXAMPLES</span></span>

### <span data-ttu-id="41f00-108">Пример 1. Создание справочного объекта группы действий в памяти</span><span class="sxs-lookup"><span data-stu-id="41f00-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperty $dict
```

## <span data-ttu-id="41f00-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="41f00-109">PARAMETERS</span></span>

### <span data-ttu-id="41f00-110">-ActionGroupId</span><span class="sxs-lookup"><span data-stu-id="41f00-110">-ActionGroupId</span></span>
<span data-ttu-id="41f00-111">ИД/имя группы действий.</span><span class="sxs-lookup"><span data-stu-id="41f00-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="41f00-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41f00-112">-DefaultProfile</span></span>
<span data-ttu-id="41f00-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="41f00-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="41f00-114">-WebhookProperty</span><span class="sxs-lookup"><span data-stu-id="41f00-114">-WebhookProperty</span></span>
<span data-ttu-id="41f00-115">Свойства веб-приложения группы действий</span><span class="sxs-lookup"><span data-stu-id="41f00-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="41f00-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f00-116">CommonParameters</span></span>
<span data-ttu-id="41f00-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41f00-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f00-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41f00-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f00-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="41f00-119">INPUTS</span></span>

### <span data-ttu-id="41f00-120">System.String</span><span class="sxs-lookup"><span data-stu-id="41f00-120">System.String</span></span>

### <span data-ttu-id="41f00-121">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="41f00-121">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="41f00-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="41f00-122">OUTPUTS</span></span>

### <span data-ttu-id="41f00-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="41f00-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="41f00-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="41f00-124">NOTES</span></span>

## <span data-ttu-id="41f00-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41f00-125">RELATED LINKS</span></span>

[<span data-ttu-id="41f00-126">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="41f00-126">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="41f00-127">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="41f00-127">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="41f00-128">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="41f00-128">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="41f00-129">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="41f00-129">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="41f00-130">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="41f00-130">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="41f00-131">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="41f00-131">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)


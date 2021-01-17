---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98424599"
---
# <span data-ttu-id="eed9f-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="eed9f-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="eed9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eed9f-102">SYNOPSIS</span></span>
<span data-ttu-id="eed9f-103">Создает новый билет в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="eed9f-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="eed9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eed9f-104">SYNTAX</span></span>

### <span data-ttu-id="eed9f-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eed9f-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eed9f-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eed9f-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eed9f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eed9f-107">DESCRIPTION</span></span>
<span data-ttu-id="eed9f-108">Добавляет новое взаимодействие клиентов в билет в службу поддержки Azure.</span><span class="sxs-lookup"><span data-stu-id="eed9f-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="eed9f-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eed9f-109">EXAMPLES</span></span>

### <span data-ttu-id="eed9f-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="eed9f-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="eed9f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eed9f-111">PARAMETERS</span></span>

### <span data-ttu-id="eed9f-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="eed9f-112">-AsJob</span></span>
<span data-ttu-id="eed9f-113">Запустите cmdlet в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="eed9f-113">Run cmdlet in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed9f-114">-Body</span><span class="sxs-lookup"><span data-stu-id="eed9f-114">-Body</span></span>
<span data-ttu-id="eed9f-115">Тело сообщения.</span><span class="sxs-lookup"><span data-stu-id="eed9f-115">Body of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eed9f-116">-DefaultProfile</span></span>
<span data-ttu-id="eed9f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eed9f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eed9f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="eed9f-118">-Name</span></span>
<span data-ttu-id="eed9f-119">Имя информационного ресурса.</span><span class="sxs-lookup"><span data-stu-id="eed9f-119">Name of the communication resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed9f-120">-Sender</span><span class="sxs-lookup"><span data-stu-id="eed9f-120">-Sender</span></span>
<span data-ttu-id="eed9f-121">Адрес электронной почты отправщика.</span><span class="sxs-lookup"><span data-stu-id="eed9f-121">Email address of the sender.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed9f-122">-Subject</span><span class="sxs-lookup"><span data-stu-id="eed9f-122">-Subject</span></span>
<span data-ttu-id="eed9f-123">Тема сообщения.</span><span class="sxs-lookup"><span data-stu-id="eed9f-123">Subject of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed9f-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="eed9f-124">-SupportTicketName</span></span>
<span data-ttu-id="eed9f-125">Имя билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="eed9f-125">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eed9f-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="eed9f-126">-SupportTicketObject</span></span>
<span data-ttu-id="eed9f-127">Объект билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="eed9f-127">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eed9f-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eed9f-128">-Confirm</span></span>
<span data-ttu-id="eed9f-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="eed9f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eed9f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eed9f-130">-WhatIf</span></span>
<span data-ttu-id="eed9f-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eed9f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eed9f-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eed9f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eed9f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eed9f-133">CommonParameters</span></span>
<span data-ttu-id="eed9f-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eed9f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eed9f-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eed9f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eed9f-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eed9f-136">INPUTS</span></span>

### <span data-ttu-id="eed9f-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="eed9f-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="eed9f-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eed9f-138">OUTPUTS</span></span>

### <span data-ttu-id="eed9f-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="eed9f-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="eed9f-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eed9f-140">NOTES</span></span>

## <span data-ttu-id="eed9f-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eed9f-141">RELATED LINKS</span></span>

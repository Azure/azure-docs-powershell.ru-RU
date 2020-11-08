---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236505"
---
# <span data-ttu-id="384f3-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="384f3-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="384f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="384f3-102">SYNOPSIS</span></span>
<span data-ttu-id="384f3-103">Создание нового общения с билетами поддержки.</span><span class="sxs-lookup"><span data-stu-id="384f3-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="384f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="384f3-104">SYNTAX</span></span>

### <span data-ttu-id="384f3-105">CreateByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="384f3-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="384f3-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="384f3-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="384f3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="384f3-107">DESCRIPTION</span></span>
<span data-ttu-id="384f3-108">Добавляет новый клиентский связь с билетом службы поддержки Azure.</span><span class="sxs-lookup"><span data-stu-id="384f3-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="384f3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="384f3-109">EXAMPLES</span></span>

### <span data-ttu-id="384f3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="384f3-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="384f3-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="384f3-111">PARAMETERS</span></span>

### <span data-ttu-id="384f3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="384f3-112">-AsJob</span></span>
<span data-ttu-id="384f3-113">Запустите командлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="384f3-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="384f3-114">-Body</span><span class="sxs-lookup"><span data-stu-id="384f3-114">-Body</span></span>
<span data-ttu-id="384f3-115">Текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="384f3-115">Body of the communication.</span></span>

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

### <span data-ttu-id="384f3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="384f3-116">-DefaultProfile</span></span>
<span data-ttu-id="384f3-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="384f3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="384f3-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="384f3-118">-Name</span></span>
<span data-ttu-id="384f3-119">Имя коммуникационного ресурса.</span><span class="sxs-lookup"><span data-stu-id="384f3-119">Name of the communication resource.</span></span>

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

### <span data-ttu-id="384f3-120">-Отправитель</span><span class="sxs-lookup"><span data-stu-id="384f3-120">-Sender</span></span>
<span data-ttu-id="384f3-121">Адрес электронной почты отправителя.</span><span class="sxs-lookup"><span data-stu-id="384f3-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="384f3-122">-Тема</span><span class="sxs-lookup"><span data-stu-id="384f3-122">-Subject</span></span>
<span data-ttu-id="384f3-123">Тема общения.</span><span class="sxs-lookup"><span data-stu-id="384f3-123">Subject of the communication.</span></span>

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

### <span data-ttu-id="384f3-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="384f3-124">-SupportTicketName</span></span>
<span data-ttu-id="384f3-125">Имя билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="384f3-125">Support ticket name.</span></span>

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

### <span data-ttu-id="384f3-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="384f3-126">-SupportTicketObject</span></span>
<span data-ttu-id="384f3-127">Объект билета в службу поддержки.</span><span class="sxs-lookup"><span data-stu-id="384f3-127">Support ticket object.</span></span>

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

### <span data-ttu-id="384f3-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="384f3-128">-Confirm</span></span>
<span data-ttu-id="384f3-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="384f3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="384f3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="384f3-130">-WhatIf</span></span>
<span data-ttu-id="384f3-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="384f3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="384f3-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="384f3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="384f3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="384f3-133">CommonParameters</span></span>
<span data-ttu-id="384f3-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="384f3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="384f3-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="384f3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="384f3-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="384f3-136">INPUTS</span></span>

### <span data-ttu-id="384f3-137">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="384f3-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="384f3-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="384f3-138">OUTPUTS</span></span>

### <span data-ttu-id="384f3-139">Microsoft. Azure. Commands. support. Models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="384f3-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="384f3-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="384f3-140">NOTES</span></span>

## <span data-ttu-id="384f3-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="384f3-141">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 35e3889603dc7e86a7d10679864adfd34a880b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732615"
---
# <span data-ttu-id="b3f16-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b3f16-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="b3f16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b3f16-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f16-103">Удаляет указанное правило авторизации центра событий.</span><span class="sxs-lookup"><span data-stu-id="b3f16-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3f16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b3f16-104">SYNTAX</span></span>

### <span data-ttu-id="b3f16-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b3f16-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3f16-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3f16-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3f16-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3f16-107">DESCRIPTION</span></span>
<span data-ttu-id="b3f16-108">Командлет Remove-AzureRmEventHubAuthorizationRule удаляет и удаляет указанное правило авторизации из заданного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="b3f16-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="b3f16-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b3f16-109">EXAMPLES</span></span>

### <span data-ttu-id="b3f16-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b3f16-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="b3f16-111">Удаляет правило авторизации \` MyAuthRuleName \` из пространства имен \` MyNamespaceName \` .</span><span class="sxs-lookup"><span data-stu-id="b3f16-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="b3f16-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b3f16-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="b3f16-113">Удаляет правило авторизации \` MyAuthRuleName \` из центра событий \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="b3f16-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="b3f16-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b3f16-114">PARAMETERS</span></span>

### <span data-ttu-id="b3f16-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f16-115">-DefaultProfile</span></span>
<span data-ttu-id="b3f16-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f16-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3f16-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b3f16-117">-EventHub</span></span>
<span data-ttu-id="b3f16-118">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="b3f16-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f16-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b3f16-119">-Force</span></span>
<span data-ttu-id="b3f16-120">Не запрашивать подтверждение</span><span class="sxs-lookup"><span data-stu-id="b3f16-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="b3f16-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b3f16-121">-Name</span></span>
<span data-ttu-id="b3f16-122">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b3f16-122">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f16-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b3f16-123">-Namespace</span></span>
<span data-ttu-id="b3f16-124">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="b3f16-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f16-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3f16-125">-PassThru</span></span>
<span data-ttu-id="b3f16-126">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b3f16-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b3f16-127">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b3f16-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b3f16-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f16-128">-ResourceGroupName</span></span>
<span data-ttu-id="b3f16-129">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b3f16-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3f16-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b3f16-130">-Confirm</span></span>
<span data-ttu-id="b3f16-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b3f16-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3f16-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3f16-132">-WhatIf</span></span>
<span data-ttu-id="b3f16-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b3f16-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3f16-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b3f16-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3f16-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f16-135">CommonParameters</span></span>
<span data-ttu-id="b3f16-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b3f16-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f16-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3f16-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f16-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b3f16-138">INPUTS</span></span>

### <span data-ttu-id="b3f16-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b3f16-139">System.String</span></span>

## <span data-ttu-id="b3f16-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b3f16-140">OUTPUTS</span></span>

### <span data-ttu-id="b3f16-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3f16-141">System.Boolean</span></span>

## <span data-ttu-id="b3f16-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b3f16-142">NOTES</span></span>

## <span data-ttu-id="b3f16-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b3f16-143">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: c15528befc90a0249101602fef9b178e7a63c0ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564944"
---
# <span data-ttu-id="03e8c-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="03e8c-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="03e8c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="03e8c-102">SYNOPSIS</span></span>
<span data-ttu-id="03e8c-103">Удаляет указанное правило авторизации центра событий.</span><span class="sxs-lookup"><span data-stu-id="03e8c-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03e8c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="03e8c-104">SYNTAX</span></span>

### <span data-ttu-id="03e8c-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="03e8c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03e8c-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="03e8c-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03e8c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="03e8c-107">DESCRIPTION</span></span>
<span data-ttu-id="03e8c-108">Командлет Remove-AzureRmEventHubAuthorizationRule удаляет и удаляет указанное правило авторизации из заданного концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="03e8c-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="03e8c-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="03e8c-109">EXAMPLES</span></span>

### <span data-ttu-id="03e8c-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="03e8c-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="03e8c-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="03e8c-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="03e8c-112">Удаляет правило авторизации \` MyAuthRuleName \` из центра событий \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="03e8c-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="03e8c-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="03e8c-113">PARAMETERS</span></span>

### <span data-ttu-id="03e8c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e8c-114">-DefaultProfile</span></span>
<span data-ttu-id="03e8c-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="03e8c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03e8c-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="03e8c-116">-EventHub</span></span>
<span data-ttu-id="03e8c-117">Имя EventHub</span><span class="sxs-lookup"><span data-stu-id="03e8c-117">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e8c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="03e8c-118">-Force</span></span>
<span data-ttu-id="03e8c-119">Не запрашивать подтверждение</span><span class="sxs-lookup"><span data-stu-id="03e8c-119">Do not ask for confirmation</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e8c-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="03e8c-120">-Name</span></span>
<span data-ttu-id="03e8c-121">Имя AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="03e8c-121">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e8c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="03e8c-122">-Namespace</span></span>
<span data-ttu-id="03e8c-123">Имя пространства имен</span><span class="sxs-lookup"><span data-stu-id="03e8c-123">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e8c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03e8c-124">-PassThru</span></span>
<span data-ttu-id="03e8c-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="03e8c-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="03e8c-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="03e8c-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e8c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03e8c-127">-ResourceGroupName</span></span>
<span data-ttu-id="03e8c-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="03e8c-128">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03e8c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03e8c-129">-Confirm</span></span>
<span data-ttu-id="03e8c-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="03e8c-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e8c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03e8c-131">-WhatIf</span></span>
<span data-ttu-id="03e8c-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="03e8c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03e8c-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="03e8c-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03e8c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e8c-134">CommonParameters</span></span>
<span data-ttu-id="03e8c-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="03e8c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="03e8c-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03e8c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e8c-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="03e8c-137">INPUTS</span></span>

### <span data-ttu-id="03e8c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="03e8c-138">System.String</span></span>


## <span data-ttu-id="03e8c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="03e8c-139">OUTPUTS</span></span>

### <span data-ttu-id="03e8c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="03e8c-140">System.Boolean</span></span>


## <span data-ttu-id="03e8c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="03e8c-141">NOTES</span></span>

## <span data-ttu-id="03e8c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="03e8c-142">RELATED LINKS</span></span>

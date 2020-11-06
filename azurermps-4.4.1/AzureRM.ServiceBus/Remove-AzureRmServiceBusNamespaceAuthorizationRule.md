---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 08f7f33138ddf9d5226cfc93f263fdec65de3388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562164"
---
# <span data-ttu-id="a3f89-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a3f89-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="a3f89-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a3f89-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f89-103">Удаляет правило авторизации из заданной группы ресурсов для пространства имен служебной шины.</span><span class="sxs-lookup"><span data-stu-id="a3f89-103">Removes the authorization rule of a Service Bus namespace from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a3f89-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a3f89-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroupName <String> -Namespace <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3f89-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3f89-105">DESCRIPTION</span></span>
<span data-ttu-id="a3f89-106">Командлет **Remove-AzureRmServiceBusNamespaceAuthorizationRule** удаляет правило авторизации из пространства имен служебной шины для указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a3f89-106">The **Remove-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace for the specified resource group.</span></span>

## <span data-ttu-id="a3f89-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a3f89-107">EXAMPLES</span></span>

### <span data-ttu-id="a3f89-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a3f89-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="a3f89-109">Удаление правила авторизации `SBAuthoRule1` пространства имен `SB-Example1` из указанной группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a3f89-109">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

## <span data-ttu-id="a3f89-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a3f89-110">PARAMETERS</span></span>

### <span data-ttu-id="a3f89-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a3f89-111">-Confirm</span></span>
<span data-ttu-id="a3f89-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a3f89-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f89-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3f89-113">-WhatIf</span></span>
<span data-ttu-id="a3f89-114">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a3f89-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3f89-115">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a3f89-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3f89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f89-116">-DefaultProfile</span></span>
<span data-ttu-id="a3f89-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a3f89-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3f89-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a3f89-118">-Name</span></span>
<span data-ttu-id="a3f89-119">AuthorizationRule имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a3f89-119">Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f89-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a3f89-120">-Namespace</span></span>
<span data-ttu-id="a3f89-121">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="a3f89-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f89-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3f89-122">-ResourceGroupName</span></span>
<span data-ttu-id="a3f89-123">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a3f89-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f89-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f89-124">CommonParameters</span></span>
<span data-ttu-id="a3f89-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a3f89-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f89-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3f89-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f89-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a3f89-127">INPUTS</span></span>

### <span data-ttu-id="a3f89-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a3f89-128">-ResourceGroup</span></span>
 <span data-ttu-id="a3f89-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a3f89-129">System.String</span></span>

### <span data-ttu-id="a3f89-130">-+ +</span><span class="sxs-lookup"><span data-stu-id="a3f89-130">-NamespaceName</span></span>
 <span data-ttu-id="a3f89-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a3f89-131">System.String</span></span>

### <span data-ttu-id="a3f89-132">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="a3f89-132">-AuthorizationRuleName</span></span>
 <span data-ttu-id="a3f89-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a3f89-133">System.String</span></span>

## <span data-ttu-id="a3f89-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a3f89-134">OUTPUTS</span></span>

### <span data-ttu-id="a3f89-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3f89-135">System.Boolean</span></span>

## <span data-ttu-id="a3f89-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="a3f89-136">NOTES</span></span>

## <span data-ttu-id="a3f89-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a3f89-137">RELATED LINKS</span></span>


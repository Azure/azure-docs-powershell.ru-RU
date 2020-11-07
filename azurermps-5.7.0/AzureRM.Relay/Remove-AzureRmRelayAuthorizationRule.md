---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 62d37b30f20cf6d0738cfc927c266d6869be5586
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733240"
---
# <span data-ttu-id="ea7c4-101">Remove-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ea7c4-101">Remove-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="ea7c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea7c4-102">SYNOPSIS</span></span>
<span data-ttu-id="ea7c4-103">Удаляет правило авторизации HybridConnection из заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ea7c4-103">Removes the authorization rule of a HybridConnection from the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea7c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea7c4-104">SYNTAX</span></span>

### <span data-ttu-id="ea7c4-105">NamespaceAuthorizationRuleSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea7c4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea7c4-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea7c4-106">WcfRelayAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea7c4-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ea7c4-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Remove-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea7c4-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea7c4-108">DESCRIPTION</span></span>
<span data-ttu-id="ea7c4-109">Командлет **Remove-AzureRmRelayAuthorizationRule** удаляет правило авторизации для заданных сущностей ретрансляции (пространство имен/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="ea7c4-109">The **Remove-AzureRmRelayAuthorizationRule** cmdlet removes the authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="ea7c4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea7c4-110">EXAMPLES</span></span>

### <span data-ttu-id="ea7c4-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ea7c4-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="ea7c4-112">Удаляет правило авторизации `AuthoRule1` для пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ea7c4-112">Removes the authorization rule `AuthoRule1` of the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="ea7c4-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="ea7c4-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWcfRelay -Name AuthoRule1
```

<span data-ttu-id="ea7c4-114">Удаляет правило авторизации `AuthoRule1` WcfRelay `TestWcfRelay` из пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ea7c4-114">Removes the authorization rule `AuthoRule1` of the WcfRelay `TestWcfRelay` from the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="ea7c4-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="ea7c4-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="ea7c4-116">Удаляет правило авторизации `AuthoRule1` HybridConnection `TestHybridConnection` из пространства имен `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="ea7c4-116">Removes the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="ea7c4-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea7c4-117">PARAMETERS</span></span>

### <span data-ttu-id="ea7c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea7c4-118">-DefaultProfile</span></span>
<span data-ttu-id="ea7c4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea7c4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="ea7c4-120">-Force</span></span>
<span data-ttu-id="ea7c4-121">Не запрашивать подтверждение</span><span class="sxs-lookup"><span data-stu-id="ea7c4-121">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="ea7c4-122">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="ea7c4-122">-HybridConnection</span></span>
<span data-ttu-id="ea7c4-123">HybridConnection имя.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-123">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea7c4-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea7c4-124">-Name</span></span>
<span data-ttu-id="ea7c4-125">AuthorizationRule имя.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-125">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea7c4-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ea7c4-126">-Namespace</span></span>
<span data-ttu-id="ea7c4-127">Имя пространства имен.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-127">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea7c4-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea7c4-128">-PassThru</span></span>
<span data-ttu-id="ea7c4-129">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="ea7c4-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ea7c4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea7c4-130">-ResourceGroupName</span></span>
<span data-ttu-id="ea7c4-131">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="ea7c4-132">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="ea7c4-132">-WcfRelay</span></span>
<span data-ttu-id="ea7c4-133">WcfRelay имя.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-133">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea7c4-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea7c4-134">-Confirm</span></span>
<span data-ttu-id="ea7c4-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea7c4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea7c4-136">-WhatIf</span></span>
<span data-ttu-id="ea7c4-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea7c4-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea7c4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea7c4-139">CommonParameters</span></span>
<span data-ttu-id="ea7c4-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea7c4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea7c4-141">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea7c4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea7c4-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea7c4-142">INPUTS</span></span>

### <span data-ttu-id="ea7c4-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ea7c4-143">System.String</span></span>

## <span data-ttu-id="ea7c4-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea7c4-144">OUTPUTS</span></span>

### <span data-ttu-id="ea7c4-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea7c4-145">System.Boolean</span></span>

## <span data-ttu-id="ea7c4-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea7c4-146">NOTES</span></span>

## <span data-ttu-id="ea7c4-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea7c4-147">RELATED LINKS</span></span>


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/remove-azpeeringregisteredasn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeeringRegisteredAsn.md
ms.openlocfilehash: d43fe033b58ba6295728bc0c21ddb1d853587b59
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246033"
---
# <span data-ttu-id="9905a-101">Remove-AzPeeringRegisteredAsn</span><span class="sxs-lookup"><span data-stu-id="9905a-101">Remove-AzPeeringRegisteredAsn</span></span>

## <span data-ttu-id="9905a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9905a-102">SYNOPSIS</span></span>
<span data-ttu-id="9905a-103">Удалите или удалите зарегистрированный ASN из родительского ресурса пиринга.</span><span class="sxs-lookup"><span data-stu-id="9905a-103">Delete or remove a registered ASN from the parent peering resource.</span></span>

## <span data-ttu-id="9905a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9905a-104">SYNTAX</span></span>

### <span data-ttu-id="9905a-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9905a-105">ByName (Default)</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String> [-Force]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9905a-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9905a-106">InputObject</span></span>
```
Remove-AzPeeringRegisteredAsn -InputObject <PSPeeringServicePrefix> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9905a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9905a-107">ByResourceId</span></span>
```
Remove-AzPeeringRegisteredAsn [-ResourceId] <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9905a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9905a-108">DESCRIPTION</span></span>
<span data-ttu-id="9905a-109">Позволяет удалять зарегистрированные ASN из родительского ресурса однорангового соединения.</span><span class="sxs-lookup"><span data-stu-id="9905a-109">Allows the removal of registered ASN from parent peering resource.</span></span>

## <span data-ttu-id="9905a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9905a-110">EXAMPLES</span></span>

### <span data-ttu-id="9905a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9905a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeeringRegisteredAsn -ResourceId $resourceId
```

<span data-ttu-id="9905a-112">Удаление регистрационного номера ASN по идентификатору ресурса.</span><span class="sxs-lookup"><span data-stu-id="9905a-112">Remove a registerd ASN by resource id.</span></span>

## <span data-ttu-id="9905a-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9905a-113">PARAMETERS</span></span>

### <span data-ttu-id="9905a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9905a-114">-AsJob</span></span>
<span data-ttu-id="9905a-115">Выполнение в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="9905a-115">Run in the background.</span></span>

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

### <span data-ttu-id="9905a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9905a-116">-DefaultProfile</span></span>
<span data-ttu-id="9905a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9905a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9905a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="9905a-118">-Force</span></span>
<span data-ttu-id="9905a-119">Принудительно завершить операцию</span><span class="sxs-lookup"><span data-stu-id="9905a-119">Force the operation to complete</span></span>

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

### <span data-ttu-id="9905a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9905a-120">-InputObject</span></span>
<span data-ttu-id="9905a-121">Использование Get-AzPeeringServicePrefix</span><span class="sxs-lookup"><span data-stu-id="9905a-121">Use a Get-AzPeeringServicePrefix</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9905a-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9905a-122">-Name</span></span>
<span data-ttu-id="9905a-123">Имя зарегистрированного ASN</span><span class="sxs-lookup"><span data-stu-id="9905a-123">The name of the registered ASN</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9905a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9905a-124">-PassThru</span></span>
<span data-ttu-id="9905a-125">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="9905a-125">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="9905a-126">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="9905a-126">-PeeringName</span></span>
<span data-ttu-id="9905a-127">Уникальное имя PSPeering.</span><span class="sxs-lookup"><span data-stu-id="9905a-127">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9905a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9905a-128">-ResourceGroupName</span></span>
<span data-ttu-id="9905a-129">Создание или использование существующего имени группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9905a-129">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9905a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9905a-130">-ResourceId</span></span>
<span data-ttu-id="9905a-131">Имя строки идентификатора ресурса.</span><span class="sxs-lookup"><span data-stu-id="9905a-131">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9905a-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9905a-132">-Confirm</span></span>
<span data-ttu-id="9905a-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9905a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9905a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9905a-134">-WhatIf</span></span>
<span data-ttu-id="9905a-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9905a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9905a-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9905a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9905a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9905a-137">CommonParameters</span></span>
<span data-ttu-id="9905a-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9905a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9905a-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9905a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9905a-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9905a-140">INPUTS</span></span>

### <span data-ttu-id="9905a-141">Microsoft. Azure. PowerShell. командлеты. Peer (Models. PSPeeringServicePrefix)</span><span class="sxs-lookup"><span data-stu-id="9905a-141">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringServicePrefix</span></span>

### <span data-ttu-id="9905a-142">System. String</span><span class="sxs-lookup"><span data-stu-id="9905a-142">System.String</span></span>

## <span data-ttu-id="9905a-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9905a-143">OUTPUTS</span></span>

### <span data-ttu-id="9905a-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9905a-144">System.Boolean</span></span>

## <span data-ttu-id="9905a-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="9905a-145">NOTES</span></span>

## <span data-ttu-id="9905a-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9905a-146">RELATED LINKS</span></span>
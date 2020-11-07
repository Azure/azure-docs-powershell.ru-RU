---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmPublicIpPrefix.md
ms.openlocfilehash: e361e4d3c4daec88ddb35fa7973b65f630dcc390
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734331"
---
# <span data-ttu-id="e49b8-101">Remove-AzureRmPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e49b8-101">Remove-AzureRmPublicIpPrefix</span></span>

## <span data-ttu-id="e49b8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e49b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e49b8-103">Удаление префикса общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="e49b8-103">Removes a public IP prefix</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e49b8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e49b8-104">SYNTAX</span></span>

### <span data-ttu-id="e49b8-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e49b8-105">RemoveByNameParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e49b8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e49b8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e49b8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e49b8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzureRmPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e49b8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e49b8-108">DESCRIPTION</span></span>
<span data-ttu-id="e49b8-109">Командлет "\* \* Remove-AzureRmPublicIpPrefix" удаляет префикс общедоступного IP-адреса Azure, так как у него нет общедоступных IP-адресов, выделены от него.</span><span class="sxs-lookup"><span data-stu-id="e49b8-109">The \*\*Remove-AzureRmPublicIpPrefix cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="e49b8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e49b8-110">EXAMPLES</span></span>

### <span data-ttu-id="e49b8-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e49b8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="e49b8-112">Удаление префикса общедоступного IP-адреса с именем $prefixName из группы ресурсов $rgName</span><span class="sxs-lookup"><span data-stu-id="e49b8-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="e49b8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e49b8-113">PARAMETERS</span></span>

### <span data-ttu-id="e49b8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e49b8-114">-AsJob</span></span>
<span data-ttu-id="e49b8-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e49b8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e49b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e49b8-116">-DefaultProfile</span></span>
<span data-ttu-id="e49b8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e49b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e49b8-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e49b8-118">-Force</span></span>
<span data-ttu-id="e49b8-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e49b8-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e49b8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e49b8-120">-InputObject</span></span>
<span data-ttu-id="e49b8-121">Объект PublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e49b8-121">A PublicIpPrefix object</span></span>

```yaml
Type: PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e49b8-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e49b8-122">-Name</span></span>
<span data-ttu-id="e49b8-123">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e49b8-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e49b8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e49b8-124">-PassThru</span></span>
<span data-ttu-id="e49b8-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e49b8-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e49b8-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e49b8-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e49b8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e49b8-127">-ResourceGroupName</span></span>
<span data-ttu-id="e49b8-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e49b8-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e49b8-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e49b8-129">-ResourceId</span></span>
<span data-ttu-id="e49b8-130">ResourceId для ресурса, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e49b8-130">The resourceId for the resource to remove</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e49b8-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e49b8-131">-Confirm</span></span>
<span data-ttu-id="e49b8-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e49b8-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e49b8-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e49b8-133">-WhatIf</span></span>
<span data-ttu-id="e49b8-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e49b8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e49b8-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e49b8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e49b8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e49b8-136">CommonParameters</span></span>
<span data-ttu-id="e49b8-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e49b8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="e49b8-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e49b8-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e49b8-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e49b8-139">INPUTS</span></span>

### <span data-ttu-id="e49b8-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e49b8-140">System.String</span></span>
<span data-ttu-id="e49b8-141">Microsoft. Azure. Commands. Network. Models. PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="e49b8-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>


## <span data-ttu-id="e49b8-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e49b8-142">OUTPUTS</span></span>

### <span data-ttu-id="e49b8-143">System. Object</span><span class="sxs-lookup"><span data-stu-id="e49b8-143">System.Object</span></span>

## <span data-ttu-id="e49b8-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e49b8-144">NOTES</span></span>

## <span data-ttu-id="e49b8-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e49b8-145">RELATED LINKS</span></span>

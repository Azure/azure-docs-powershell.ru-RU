---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1CE08F0F-A59E-46AC-B470-F1DCCD46513E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworkpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzVirtualNetworkPeering.md
ms.openlocfilehash: 3bc816f690f39b534a134e80df1a86c7bbca5dc1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911097"
---
# <span data-ttu-id="217fa-101">Remove-AzVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="217fa-101">Remove-AzVirtualNetworkPeering</span></span>

## <span data-ttu-id="217fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="217fa-102">SYNOPSIS</span></span>

## <span data-ttu-id="217fa-103">Максимальное</span><span class="sxs-lookup"><span data-stu-id="217fa-103">SYNTAX</span></span>

```
Remove-AzVirtualNetworkPeering -VirtualNetworkName <String> -Name <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="217fa-104">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="217fa-104">DESCRIPTION</span></span>

## <span data-ttu-id="217fa-105">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="217fa-105">EXAMPLES</span></span>

### <span data-ttu-id="217fa-106">Пример 1: удаление пиринга виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="217fa-106">Example 1: Remove a virtual network peering</span></span>
```
# Remove the virtual network peering named myVnet1TomyVnet2 located in myVnet1 in the resource group named myResourceGroup.

Remove-AzVirtualNetworkPeering -Name "myVnet1TomyVnet2" -VirtualNetworkName "myVnet" -ResourceGroupName "myResourceGroup"
```

## <span data-ttu-id="217fa-107">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="217fa-107">PARAMETERS</span></span>

### <span data-ttu-id="217fa-108">-AsJob</span><span class="sxs-lookup"><span data-stu-id="217fa-108">-AsJob</span></span>
<span data-ttu-id="217fa-109">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="217fa-109">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="217fa-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="217fa-110">-DefaultProfile</span></span>
<span data-ttu-id="217fa-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="217fa-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="217fa-112">-Force</span><span class="sxs-lookup"><span data-stu-id="217fa-112">-Force</span></span>
<span data-ttu-id="217fa-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="217fa-113">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="217fa-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="217fa-114">-Name</span></span>
<span data-ttu-id="217fa-115">Имя пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="217fa-115">The virtual network peering name.</span></span>

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

### <span data-ttu-id="217fa-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="217fa-116">-PassThru</span></span>
<span data-ttu-id="217fa-117">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="217fa-117">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="217fa-118">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="217fa-118">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="217fa-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="217fa-119">-ResourceGroupName</span></span>
<span data-ttu-id="217fa-120">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="217fa-120">The resource group name</span></span>

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

### <span data-ttu-id="217fa-121">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="217fa-121">-VirtualNetworkName</span></span>
<span data-ttu-id="217fa-122">Имя виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="217fa-122">The virtual network name.</span></span>

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

### <span data-ttu-id="217fa-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="217fa-123">-Confirm</span></span>
<span data-ttu-id="217fa-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="217fa-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217fa-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="217fa-125">-WhatIf</span></span>
<span data-ttu-id="217fa-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="217fa-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="217fa-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="217fa-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="217fa-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="217fa-128">CommonParameters</span></span>
<span data-ttu-id="217fa-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="217fa-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="217fa-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="217fa-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="217fa-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="217fa-131">INPUTS</span></span>

## <span data-ttu-id="217fa-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="217fa-132">OUTPUTS</span></span>

## <span data-ttu-id="217fa-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="217fa-133">NOTES</span></span>

## <span data-ttu-id="217fa-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="217fa-134">RELATED LINKS</span></span>


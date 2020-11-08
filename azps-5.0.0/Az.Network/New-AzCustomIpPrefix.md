---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248549"
---
# <span data-ttu-id="63457-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="63457-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="63457-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63457-102">SYNOPSIS</span></span>
<span data-ttu-id="63457-103">Создание ресурса CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="63457-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="63457-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63457-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63457-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63457-105">DESCRIPTION</span></span>
<span data-ttu-id="63457-106">Командлет **New-AzCustomIpPrefix** создает ресурс CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="63457-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="63457-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63457-107">EXAMPLES</span></span>

### <span data-ttu-id="63457-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63457-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="63457-109">Эта команда создает новый ресурс CustomIpPrefix с именем $prefixName в группе ресурсов $rgName с CIDR 40.40.40.0/24 в westus</span><span class="sxs-lookup"><span data-stu-id="63457-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="63457-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63457-110">PARAMETERS</span></span>

### <span data-ttu-id="63457-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63457-111">-AsJob</span></span>
<span data-ttu-id="63457-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="63457-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63457-113">-CIDR</span><span class="sxs-lookup"><span data-stu-id="63457-113">-Cidr</span></span>
<span data-ttu-id="63457-114">CustomIpPrefix CIDR.</span><span class="sxs-lookup"><span data-stu-id="63457-114">The CustomIpPrefix CIDR.</span></span>

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

### <span data-ttu-id="63457-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63457-115">-DefaultProfile</span></span>
<span data-ttu-id="63457-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63457-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63457-117">-Location</span><span class="sxs-lookup"><span data-stu-id="63457-117">-Location</span></span>
<span data-ttu-id="63457-118">Расположение CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="63457-118">The CustomIpPrefix location.</span></span>

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

### <span data-ttu-id="63457-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63457-119">-Name</span></span>
<span data-ttu-id="63457-120">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="63457-120">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63457-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63457-121">-ResourceGroupName</span></span>
<span data-ttu-id="63457-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63457-122">The resource group name.</span></span>

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

### <span data-ttu-id="63457-123">-Тег</span><span class="sxs-lookup"><span data-stu-id="63457-123">-Tag</span></span>
<span data-ttu-id="63457-124">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63457-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63457-125">-Zone</span><span class="sxs-lookup"><span data-stu-id="63457-125">-Zone</span></span>
<span data-ttu-id="63457-126">Список зон доступности, обозначающих IP-адрес, выделенный для ресурса, должен быть от него.</span><span class="sxs-lookup"><span data-stu-id="63457-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63457-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63457-127">-Confirm</span></span>
<span data-ttu-id="63457-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63457-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63457-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63457-129">-WhatIf</span></span>
<span data-ttu-id="63457-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63457-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63457-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63457-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63457-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63457-132">CommonParameters</span></span>
<span data-ttu-id="63457-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63457-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63457-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63457-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63457-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63457-135">INPUTS</span></span>

### <span data-ttu-id="63457-136">System. String</span><span class="sxs-lookup"><span data-stu-id="63457-136">System.String</span></span>

### <span data-ttu-id="63457-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="63457-137">System.String[]</span></span>

### <span data-ttu-id="63457-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="63457-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="63457-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63457-139">OUTPUTS</span></span>

### <span data-ttu-id="63457-140">Microsoft. Azure. Commands. Network. Models. PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="63457-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="63457-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="63457-141">NOTES</span></span>

## <span data-ttu-id="63457-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63457-142">RELATED LINKS</span></span>

[<span data-ttu-id="63457-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="63457-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="63457-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="63457-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="63457-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="63457-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)
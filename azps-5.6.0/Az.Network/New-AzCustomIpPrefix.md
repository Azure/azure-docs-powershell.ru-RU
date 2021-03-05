---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 0ac12ba420231d34c5ad278a8fd2a091fe4982da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960403"
---
# <span data-ttu-id="04793-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="04793-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="04793-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04793-102">SYNOPSIS</span></span>
<span data-ttu-id="04793-103">Создание ресурса CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="04793-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="04793-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="04793-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04793-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04793-105">DESCRIPTION</span></span>
<span data-ttu-id="04793-106">Для **создания пользовательского ресурса CustomIpPrefix создается cmdlet New-AzCustomIpPrefix.**</span><span class="sxs-lookup"><span data-stu-id="04793-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="04793-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="04793-107">EXAMPLES</span></span>

### <span data-ttu-id="04793-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="04793-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="04793-109">Эта команда создает новый ресурс CustomIpPrefix с именем $prefixName в группе ресурсов $rgName со ссылкой 40.40.40.0/24 in westus</span><span class="sxs-lookup"><span data-stu-id="04793-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="04793-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04793-110">PARAMETERS</span></span>

### <span data-ttu-id="04793-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04793-111">-AsJob</span></span>
<span data-ttu-id="04793-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="04793-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04793-113">-Cidr</span><span class="sxs-lookup"><span data-stu-id="04793-113">-Cidr</span></span>
<span data-ttu-id="04793-114">The CustomIpPrefix CIDR.</span><span class="sxs-lookup"><span data-stu-id="04793-114">The CustomIpPrefix CIDR.</span></span>

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

### <span data-ttu-id="04793-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04793-115">-DefaultProfile</span></span>
<span data-ttu-id="04793-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="04793-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04793-117">-Location</span><span class="sxs-lookup"><span data-stu-id="04793-117">-Location</span></span>
<span data-ttu-id="04793-118">Расположение CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="04793-118">The CustomIpPrefix location.</span></span>

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

### <span data-ttu-id="04793-119">-Name</span><span class="sxs-lookup"><span data-stu-id="04793-119">-Name</span></span>
<span data-ttu-id="04793-120">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="04793-120">The resource name.</span></span>

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

### <span data-ttu-id="04793-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04793-121">-ResourceGroupName</span></span>
<span data-ttu-id="04793-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="04793-122">The resource group name.</span></span>

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

### <span data-ttu-id="04793-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="04793-123">-Tag</span></span>
<span data-ttu-id="04793-124">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="04793-124">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="04793-125">-Zone</span><span class="sxs-lookup"><span data-stu-id="04793-125">-Zone</span></span>
<span data-ttu-id="04793-126">Список зон доступности, обозначающий IP-адрес, выделенный для ресурса.</span><span class="sxs-lookup"><span data-stu-id="04793-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="04793-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04793-127">-Confirm</span></span>
<span data-ttu-id="04793-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04793-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04793-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04793-129">-WhatIf</span></span>
<span data-ttu-id="04793-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04793-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04793-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="04793-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04793-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04793-132">CommonParameters</span></span>
<span data-ttu-id="04793-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04793-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04793-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="04793-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04793-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="04793-135">INPUTS</span></span>

### <span data-ttu-id="04793-136">System.String</span><span class="sxs-lookup"><span data-stu-id="04793-136">System.String</span></span>

### <span data-ttu-id="04793-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="04793-137">System.String[]</span></span>

### <span data-ttu-id="04793-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="04793-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="04793-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="04793-139">OUTPUTS</span></span>

### <span data-ttu-id="04793-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="04793-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="04793-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="04793-141">NOTES</span></span>

## <span data-ttu-id="04793-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04793-142">RELATED LINKS</span></span>

[<span data-ttu-id="04793-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="04793-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="04793-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="04793-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="04793-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="04793-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)
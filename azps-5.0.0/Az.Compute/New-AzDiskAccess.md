---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317252"
---
# <span data-ttu-id="45c3e-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="45c3e-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="45c3e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="45c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="45c3e-103">Создание ресурса для доступа к диску</span><span class="sxs-lookup"><span data-stu-id="45c3e-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="45c3e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="45c3e-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45c3e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45c3e-105">DESCRIPTION</span></span>
<span data-ttu-id="45c3e-106">Командлет **New-AzDiskAccess** создает ресурс доступа к диску</span><span class="sxs-lookup"><span data-stu-id="45c3e-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="45c3e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="45c3e-107">EXAMPLES</span></span>

### <span data-ttu-id="45c3e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45c3e-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="45c3e-109">Эта команда создаст доступ к диску с заданными свойствами.</span><span class="sxs-lookup"><span data-stu-id="45c3e-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="45c3e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="45c3e-110">PARAMETERS</span></span>

### <span data-ttu-id="45c3e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45c3e-111">-AsJob</span></span>
<span data-ttu-id="45c3e-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="45c3e-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45c3e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c3e-113">-DefaultProfile</span></span>
<span data-ttu-id="45c3e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45c3e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45c3e-115">-Location</span><span class="sxs-lookup"><span data-stu-id="45c3e-115">-Location</span></span>
<span data-ttu-id="45c3e-116">Задает расположение.</span><span class="sxs-lookup"><span data-stu-id="45c3e-116">Specifies the location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45c3e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="45c3e-117">-Name</span></span>
<span data-ttu-id="45c3e-118">Указывает имя доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="45c3e-118">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c3e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c3e-119">-ResourceGroupName</span></span>
<span data-ttu-id="45c3e-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45c3e-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="45c3e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45c3e-121">-Confirm</span></span>
<span data-ttu-id="45c3e-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="45c3e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45c3e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45c3e-123">-WhatIf</span></span>
<span data-ttu-id="45c3e-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="45c3e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45c3e-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="45c3e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45c3e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c3e-126">CommonParameters</span></span>
<span data-ttu-id="45c3e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="45c3e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c3e-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45c3e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c3e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="45c3e-129">INPUTS</span></span>

### <span data-ttu-id="45c3e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="45c3e-130">System.String</span></span>

## <span data-ttu-id="45c3e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="45c3e-131">OUTPUTS</span></span>

### <span data-ttu-id="45c3e-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="45c3e-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="45c3e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="45c3e-133">NOTES</span></span>

## <span data-ttu-id="45c3e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45c3e-134">RELATED LINKS</span></span>

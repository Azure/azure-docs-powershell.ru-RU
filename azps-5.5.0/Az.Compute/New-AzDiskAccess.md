---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzDiskAccess.md
ms.openlocfilehash: 430c0d09c56aa4fb57399c97714dc70cb19dd500
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244120"
---
# <span data-ttu-id="6fbfe-101">New-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="6fbfe-101">New-AzDiskAccess</span></span>

## <span data-ttu-id="6fbfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fbfe-102">SYNOPSIS</span></span>
<span data-ttu-id="6fbfe-103">Создание ресурса дискового доступа</span><span class="sxs-lookup"><span data-stu-id="6fbfe-103">Creates a Disk Access resource</span></span>

## <span data-ttu-id="6fbfe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6fbfe-104">SYNTAX</span></span>

```
New-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fbfe-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6fbfe-105">DESCRIPTION</span></span>
<span data-ttu-id="6fbfe-106">Для создания ресурса Дискового доступа создается **cmdlet New-AzDiskAccess.**</span><span class="sxs-lookup"><span data-stu-id="6fbfe-106">The **New-AzDiskAccess** cmdlet creates a Disk Access resource</span></span>

## <span data-ttu-id="6fbfe-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6fbfe-107">EXAMPLES</span></span>

### <span data-ttu-id="6fbfe-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6fbfe-108">Example 1</span></span>
```
PS C:\> New-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" -Location "NorthCentralUS"
```

<span data-ttu-id="6fbfe-109">Эта команда создает дисковый доступ с заданными свойствами.</span><span class="sxs-lookup"><span data-stu-id="6fbfe-109">This command will create a Disk Access with given properties.</span></span> 

## <span data-ttu-id="6fbfe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fbfe-110">PARAMETERS</span></span>

### <span data-ttu-id="6fbfe-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6fbfe-111">-AsJob</span></span>
<span data-ttu-id="6fbfe-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6fbfe-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fbfe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fbfe-113">-DefaultProfile</span></span>
<span data-ttu-id="6fbfe-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6fbfe-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fbfe-115">-Location</span><span class="sxs-lookup"><span data-stu-id="6fbfe-115">-Location</span></span>
<span data-ttu-id="6fbfe-116">Определяет расположение.</span><span class="sxs-lookup"><span data-stu-id="6fbfe-116">Specifies the location.</span></span>

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

### <span data-ttu-id="6fbfe-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6fbfe-117">-Name</span></span>
<span data-ttu-id="6fbfe-118">Указывает имя доступа к диску.</span><span class="sxs-lookup"><span data-stu-id="6fbfe-118">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="6fbfe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fbfe-119">-ResourceGroupName</span></span>
<span data-ttu-id="6fbfe-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6fbfe-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6fbfe-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6fbfe-121">-Confirm</span></span>
<span data-ttu-id="6fbfe-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6fbfe-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fbfe-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fbfe-123">-WhatIf</span></span>
<span data-ttu-id="6fbfe-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fbfe-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fbfe-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6fbfe-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fbfe-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fbfe-126">CommonParameters</span></span>
<span data-ttu-id="6fbfe-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fbfe-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fbfe-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fbfe-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fbfe-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6fbfe-129">INPUTS</span></span>

### <span data-ttu-id="6fbfe-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6fbfe-130">System.String</span></span>

## <span data-ttu-id="6fbfe-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6fbfe-131">OUTPUTS</span></span>

### <span data-ttu-id="6fbfe-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDIskAccess</span><span class="sxs-lookup"><span data-stu-id="6fbfe-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="6fbfe-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6fbfe-133">NOTES</span></span>

## <span data-ttu-id="6fbfe-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6fbfe-134">RELATED LINKS</span></span>

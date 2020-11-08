---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 614250a7fea7091f6098b44750f4c1b471d82d8b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064821"
---
# <span data-ttu-id="93ea5-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="93ea5-101">Remove-AzImage</span></span>

## <span data-ttu-id="93ea5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93ea5-102">SYNOPSIS</span></span>
<span data-ttu-id="93ea5-103">Удаление изображения.</span><span class="sxs-lookup"><span data-stu-id="93ea5-103">Removes an image.</span></span>

## <span data-ttu-id="93ea5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93ea5-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93ea5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93ea5-105">DESCRIPTION</span></span>
<span data-ttu-id="93ea5-106">Командлет **Remove-AzImage** удаляет изображение..</span><span class="sxs-lookup"><span data-stu-id="93ea5-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="93ea5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93ea5-107">EXAMPLES</span></span>

### <span data-ttu-id="93ea5-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="93ea5-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="93ea5-109">Эта команда удаляет изображение с именем "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="93ea5-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="93ea5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93ea5-110">PARAMETERS</span></span>

### <span data-ttu-id="93ea5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93ea5-111">-AsJob</span></span>
<span data-ttu-id="93ea5-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="93ea5-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="93ea5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ea5-113">-DefaultProfile</span></span>
<span data-ttu-id="93ea5-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93ea5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93ea5-115">-Force</span><span class="sxs-lookup"><span data-stu-id="93ea5-115">-Force</span></span>
<span data-ttu-id="93ea5-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="93ea5-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93ea5-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="93ea5-117">-ImageName</span></span>
<span data-ttu-id="93ea5-118">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="93ea5-118">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93ea5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93ea5-119">-ResourceGroupName</span></span>
<span data-ttu-id="93ea5-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="93ea5-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="93ea5-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93ea5-121">-Confirm</span></span>
<span data-ttu-id="93ea5-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="93ea5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ea5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ea5-123">-WhatIf</span></span>
<span data-ttu-id="93ea5-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="93ea5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93ea5-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="93ea5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ea5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ea5-126">CommonParameters</span></span>
<span data-ttu-id="93ea5-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93ea5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ea5-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93ea5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ea5-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93ea5-129">INPUTS</span></span>

### <span data-ttu-id="93ea5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="93ea5-130">System.String</span></span>

## <span data-ttu-id="93ea5-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93ea5-131">OUTPUTS</span></span>

### <span data-ttu-id="93ea5-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="93ea5-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="93ea5-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="93ea5-133">NOTES</span></span>

## <span data-ttu-id="93ea5-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93ea5-134">RELATED LINKS</span></span>

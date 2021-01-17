---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzImage.md
ms.openlocfilehash: 614250a7fea7091f6098b44750f4c1b471d82d8b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98414263"
---
# <span data-ttu-id="6af9f-101">Remove-AzImage</span><span class="sxs-lookup"><span data-stu-id="6af9f-101">Remove-AzImage</span></span>

## <span data-ttu-id="6af9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6af9f-102">SYNOPSIS</span></span>
<span data-ttu-id="6af9f-103">Удаляет изображение.</span><span class="sxs-lookup"><span data-stu-id="6af9f-103">Removes an image.</span></span>

## <span data-ttu-id="6af9f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6af9f-104">SYNTAX</span></span>

```
Remove-AzImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6af9f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6af9f-105">DESCRIPTION</span></span>
<span data-ttu-id="6af9f-106">При **этом удаляется** изображение.</span><span class="sxs-lookup"><span data-stu-id="6af9f-106">The **Remove-AzImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="6af9f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6af9f-107">EXAMPLES</span></span>

### <span data-ttu-id="6af9f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6af9f-108">Example 1</span></span>
```
PS C:\> Remove-AzImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="6af9f-109">Эта команда удаляет изображение с именем "Изображение01" в группе ресурсов "Группа ресурсов01".</span><span class="sxs-lookup"><span data-stu-id="6af9f-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="6af9f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6af9f-110">PARAMETERS</span></span>

### <span data-ttu-id="6af9f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6af9f-111">-AsJob</span></span>
<span data-ttu-id="6af9f-112">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="6af9f-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6af9f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6af9f-113">-DefaultProfile</span></span>
<span data-ttu-id="6af9f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6af9f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6af9f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6af9f-115">-Force</span></span>
<span data-ttu-id="6af9f-116">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6af9f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6af9f-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="6af9f-117">-ImageName</span></span>
<span data-ttu-id="6af9f-118">Определяет имя изображения.</span><span class="sxs-lookup"><span data-stu-id="6af9f-118">Specifies the name of an image.</span></span>

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

### <span data-ttu-id="6af9f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6af9f-119">-ResourceGroupName</span></span>
<span data-ttu-id="6af9f-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6af9f-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6af9f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6af9f-121">-Confirm</span></span>
<span data-ttu-id="6af9f-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6af9f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6af9f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6af9f-123">-WhatIf</span></span>
<span data-ttu-id="6af9f-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6af9f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6af9f-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6af9f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6af9f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6af9f-126">CommonParameters</span></span>
<span data-ttu-id="6af9f-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6af9f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6af9f-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6af9f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6af9f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6af9f-129">INPUTS</span></span>

### <span data-ttu-id="6af9f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6af9f-130">System.String</span></span>

## <span data-ttu-id="6af9f-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6af9f-131">OUTPUTS</span></span>

### <span data-ttu-id="6af9f-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="6af9f-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="6af9f-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6af9f-133">NOTES</span></span>

## <span data-ttu-id="6af9f-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6af9f-134">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmImage.md
ms.openlocfilehash: 8a1af49923c275d0f4d8fbe25a5aaaa28dbaa512
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561019"
---
# <span data-ttu-id="e666d-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="e666d-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="e666d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e666d-102">SYNOPSIS</span></span>
<span data-ttu-id="e666d-103">Удаление изображения.</span><span class="sxs-lookup"><span data-stu-id="e666d-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e666d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e666d-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e666d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e666d-105">DESCRIPTION</span></span>
<span data-ttu-id="e666d-106">Командлет **Remove-AzureRmImage** удаляет изображение..</span><span class="sxs-lookup"><span data-stu-id="e666d-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="e666d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e666d-107">EXAMPLES</span></span>

### <span data-ttu-id="e666d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e666d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="e666d-109">Эта команда удаляет изображение с именем "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="e666d-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="e666d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e666d-110">PARAMETERS</span></span>

### <span data-ttu-id="e666d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e666d-111">-AsJob</span></span>
<span data-ttu-id="e666d-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="e666d-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="e666d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e666d-113">-DefaultProfile</span></span>
<span data-ttu-id="e666d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e666d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e666d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e666d-115">-Force</span></span>
<span data-ttu-id="e666d-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="e666d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e666d-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="e666d-117">-ImageName</span></span>
<span data-ttu-id="e666d-118">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="e666d-118">Specifies the name of an image.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e666d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e666d-119">-ResourceGroupName</span></span>
<span data-ttu-id="e666d-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e666d-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e666d-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e666d-121">-Confirm</span></span>
<span data-ttu-id="e666d-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e666d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e666d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e666d-123">-WhatIf</span></span>
<span data-ttu-id="e666d-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e666d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e666d-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e666d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e666d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e666d-126">CommonParameters</span></span>
<span data-ttu-id="e666d-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e666d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e666d-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e666d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e666d-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e666d-129">INPUTS</span></span>

### <span data-ttu-id="e666d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e666d-130">System.String</span></span>

## <span data-ttu-id="e666d-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e666d-131">OUTPUTS</span></span>

### <span data-ttu-id="e666d-132">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="e666d-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="e666d-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e666d-133">NOTES</span></span>

## <span data-ttu-id="e666d-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e666d-134">RELATED LINKS</span></span>

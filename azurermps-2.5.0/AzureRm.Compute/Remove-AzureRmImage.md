---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermimage
schema: 2.0.0
ms.openlocfilehash: 5e52e75ea1af799eb2640e38cfa0e053b6b3cc7d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914545"
---
# <span data-ttu-id="d1422-101">Remove-AzureRmImage</span><span class="sxs-lookup"><span data-stu-id="d1422-101">Remove-AzureRmImage</span></span>

## <span data-ttu-id="d1422-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d1422-102">SYNOPSIS</span></span>
<span data-ttu-id="d1422-103">Удаление изображения.</span><span class="sxs-lookup"><span data-stu-id="d1422-103">Removes an image.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1422-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d1422-104">SYNTAX</span></span>

```
Remove-AzureRmImage [-ResourceGroupName] <String> [-ImageName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1422-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1422-105">DESCRIPTION</span></span>
<span data-ttu-id="d1422-106">Командлет **Remove-AzureRmImage** удаляет изображение..</span><span class="sxs-lookup"><span data-stu-id="d1422-106">The **Remove-AzureRmImage** cmdlet removes an image..</span></span>

## <span data-ttu-id="d1422-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d1422-107">EXAMPLES</span></span>

### <span data-ttu-id="d1422-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d1422-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmImage -ResourceGroupName 'ResourceGroup01' -ImageName 'Image01' -Force;
```

<span data-ttu-id="d1422-109">Эта команда удаляет изображение с именем "image01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="d1422-109">This command removes the image named 'Image01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="d1422-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d1422-110">PARAMETERS</span></span>

### <span data-ttu-id="d1422-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1422-111">-AsJob</span></span>
<span data-ttu-id="d1422-112">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="d1422-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="d1422-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1422-113">-DefaultProfile</span></span>
<span data-ttu-id="d1422-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1422-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1422-115">-Force</span><span class="sxs-lookup"><span data-stu-id="d1422-115">-Force</span></span>
<span data-ttu-id="d1422-116">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="d1422-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d1422-117">-ImageName</span><span class="sxs-lookup"><span data-stu-id="d1422-117">-ImageName</span></span>
<span data-ttu-id="d1422-118">Указывает имя изображения.</span><span class="sxs-lookup"><span data-stu-id="d1422-118">Specifies the name of an image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1422-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1422-119">-ResourceGroupName</span></span>
<span data-ttu-id="d1422-120">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1422-120">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1422-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1422-121">-Confirm</span></span>
<span data-ttu-id="d1422-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d1422-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1422-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1422-123">-WhatIf</span></span>
<span data-ttu-id="d1422-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d1422-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1422-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d1422-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1422-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1422-126">CommonParameters</span></span>
<span data-ttu-id="d1422-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d1422-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1422-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1422-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1422-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d1422-129">INPUTS</span></span>

### <span data-ttu-id="d1422-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d1422-130">System.String</span></span>

## <span data-ttu-id="d1422-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1422-131">OUTPUTS</span></span>

### <span data-ttu-id="d1422-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="d1422-132">System.Object</span></span>

## <span data-ttu-id="d1422-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d1422-133">NOTES</span></span>

## <span data-ttu-id="d1422-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1422-134">RELATED LINKS</span></span>


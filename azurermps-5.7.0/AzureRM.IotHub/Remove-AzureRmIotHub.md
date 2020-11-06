---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/remove-azurermiothub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Remove-AzureRmIotHub.md
ms.openlocfilehash: 1da7b9981b3c2fe96d895290b7ab73dfc36e183e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564864"
---
# <span data-ttu-id="15339-101">Remove-AzureRmIotHub</span><span class="sxs-lookup"><span data-stu-id="15339-101">Remove-AzureRmIotHub</span></span>

## <span data-ttu-id="15339-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15339-102">SYNOPSIS</span></span>
<span data-ttu-id="15339-103">Удаление IotHub.</span><span class="sxs-lookup"><span data-stu-id="15339-103">Deletes an IotHub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15339-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15339-104">SYNTAX</span></span>

```
Remove-AzureRmIotHub [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15339-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15339-105">DESCRIPTION</span></span>
<span data-ttu-id="15339-106">Удаление IotHub.</span><span class="sxs-lookup"><span data-stu-id="15339-106">Deletes an IotHub.</span></span>

## <span data-ttu-id="15339-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15339-107">EXAMPLES</span></span>

### <span data-ttu-id="15339-108">Пример 1 удаление IotHub</span><span class="sxs-lookup"><span data-stu-id="15339-108">Example 1 Remove an IotHub</span></span>
```
PS C:\> Remove-AzureRmIotHub -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="15339-109">Удаляет IotHub с именем "myiothub"</span><span class="sxs-lookup"><span data-stu-id="15339-109">Removes an IotHub named "myiothub"</span></span>

## <span data-ttu-id="15339-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15339-110">PARAMETERS</span></span>

### <span data-ttu-id="15339-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15339-111">-DefaultProfile</span></span>
<span data-ttu-id="15339-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="15339-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15339-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="15339-113">-Name</span></span>
<span data-ttu-id="15339-114">Имя IotHub</span><span class="sxs-lookup"><span data-stu-id="15339-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="15339-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15339-115">-ResourceGroupName</span></span>
<span data-ttu-id="15339-116">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="15339-116">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15339-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15339-117">-Confirm</span></span>
<span data-ttu-id="15339-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15339-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15339-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15339-119">-WhatIf</span></span>
<span data-ttu-id="15339-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15339-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15339-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15339-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15339-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15339-122">CommonParameters</span></span>
<span data-ttu-id="15339-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15339-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15339-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15339-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15339-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15339-125">INPUTS</span></span>

### <span data-ttu-id="15339-126">System. String</span><span class="sxs-lookup"><span data-stu-id="15339-126">System.String</span></span>

## <span data-ttu-id="15339-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15339-127">OUTPUTS</span></span>

### <span data-ttu-id="15339-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="15339-128">System.Object</span></span>

## <span data-ttu-id="15339-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="15339-129">NOTES</span></span>

## <span data-ttu-id="15339-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15339-130">RELATED LINKS</span></span>


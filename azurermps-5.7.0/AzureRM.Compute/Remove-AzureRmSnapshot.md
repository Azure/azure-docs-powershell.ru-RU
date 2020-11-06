---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmSnapshot.md
ms.openlocfilehash: 36dec1f8d4374f2e5bbed1f742aa7733bb760f67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563675"
---
# <span data-ttu-id="1992b-101">Remove-AzureRmSnapshot</span><span class="sxs-lookup"><span data-stu-id="1992b-101">Remove-AzureRmSnapshot</span></span>

## <span data-ttu-id="1992b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1992b-102">SYNOPSIS</span></span>
<span data-ttu-id="1992b-103">Удаляет снимок.</span><span class="sxs-lookup"><span data-stu-id="1992b-103">Removes a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1992b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1992b-104">SYNTAX</span></span>

```
Remove-AzureRmSnapshot [-ResourceGroupName] <String> [-SnapshotName] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1992b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1992b-105">DESCRIPTION</span></span>
<span data-ttu-id="1992b-106">Командлет **Remove-AzureRmSnapshot** удаляет моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="1992b-106">The **Remove-AzureRmSnapshot** cmdlet removes a snapshot.</span></span>

## <span data-ttu-id="1992b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1992b-107">EXAMPLES</span></span>

### <span data-ttu-id="1992b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1992b-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmSnapshot -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01' -Force;
```

<span data-ttu-id="1992b-109">Эта команда удаляет моментальный снимок с именем "Snapshot01" в группе ресурсов "ResourceGroup01".</span><span class="sxs-lookup"><span data-stu-id="1992b-109">This command removes the snapshot named 'Snapshot01' in the resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="1992b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1992b-110">PARAMETERS</span></span>

### <span data-ttu-id="1992b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="1992b-111">-Force</span></span>
<span data-ttu-id="1992b-112">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1992b-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1992b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1992b-113">-ResourceGroupName</span></span>
<span data-ttu-id="1992b-114">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1992b-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1992b-115">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="1992b-115">-SnapshotName</span></span>
<span data-ttu-id="1992b-116">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="1992b-116">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="1992b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1992b-117">-Confirm</span></span>
<span data-ttu-id="1992b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1992b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1992b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1992b-119">-WhatIf</span></span>
<span data-ttu-id="1992b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1992b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1992b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1992b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1992b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1992b-122">CommonParameters</span></span>
<span data-ttu-id="1992b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1992b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1992b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1992b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1992b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1992b-125">INPUTS</span></span>

### <span data-ttu-id="1992b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="1992b-126">System.String</span></span>

## <span data-ttu-id="1992b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1992b-127">OUTPUTS</span></span>

### <span data-ttu-id="1992b-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="1992b-128">System.Object</span></span>

## <span data-ttu-id="1992b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="1992b-129">NOTES</span></span>

## <span data-ttu-id="1992b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1992b-130">RELATED LINKS</span></span>


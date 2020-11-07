---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Revoke-AzureRmSnapshotAccess.md
ms.openlocfilehash: d081218a17bd5cac99256918d40ece722b73a85b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734468"
---
# <span data-ttu-id="dfc57-101">Revoke-AzureRmSnapshotAccess</span><span class="sxs-lookup"><span data-stu-id="dfc57-101">Revoke-AzureRmSnapshotAccess</span></span>

## <span data-ttu-id="dfc57-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="dfc57-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc57-103">Отменяет доступ к снимку.</span><span class="sxs-lookup"><span data-stu-id="dfc57-103">Revokes an access to a snapshot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dfc57-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="dfc57-104">SYNTAX</span></span>

```
Revoke-AzureRmSnapshotAccess [-ResourceGroupName] <String> [-SnapshotName] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfc57-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfc57-105">DESCRIPTION</span></span>
<span data-ttu-id="dfc57-106">Командлет **REVOKE-AzureRmSnapshotAccess** отменяет доступ к моментальному снимку.</span><span class="sxs-lookup"><span data-stu-id="dfc57-106">The **Revoke-AzureRmSnapshotAccess** cmdlet revokes an access to a snapshot.</span></span>

## <span data-ttu-id="dfc57-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="dfc57-107">EXAMPLES</span></span>

### <span data-ttu-id="dfc57-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dfc57-108">Example 1</span></span>
```
PS C:\> Revoke-AzureRmDiskAccess -ResourceGroupName 'ResourceGroup01' -SnapshotName 'Snapshot01'
```

<span data-ttu-id="dfc57-109">Отмена доступа к моментальному снимку с именем "Snapshot01" в группе ресурсов с именем "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="dfc57-109">Revoke the access to the snapshot named 'Snapshot01' in the resource group named 'ResourceGroup01'</span></span>

## <span data-ttu-id="dfc57-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="dfc57-110">PARAMETERS</span></span>

### <span data-ttu-id="dfc57-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfc57-111">-ResourceGroupName</span></span>
<span data-ttu-id="dfc57-112">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dfc57-112">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="dfc57-113">-SnapshotName</span><span class="sxs-lookup"><span data-stu-id="dfc57-113">-SnapshotName</span></span>
<span data-ttu-id="dfc57-114">Указывает имя снимка.</span><span class="sxs-lookup"><span data-stu-id="dfc57-114">Specifies the name of a snapshot.</span></span>

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

### <span data-ttu-id="dfc57-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dfc57-115">-Confirm</span></span>
<span data-ttu-id="dfc57-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="dfc57-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfc57-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfc57-117">-WhatIf</span></span>
<span data-ttu-id="dfc57-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="dfc57-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dfc57-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="dfc57-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfc57-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc57-120">CommonParameters</span></span>
<span data-ttu-id="dfc57-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="dfc57-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc57-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfc57-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc57-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="dfc57-123">INPUTS</span></span>

### <span data-ttu-id="dfc57-124">System. String</span><span class="sxs-lookup"><span data-stu-id="dfc57-124">System.String</span></span>

## <span data-ttu-id="dfc57-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="dfc57-125">OUTPUTS</span></span>

### <span data-ttu-id="dfc57-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="dfc57-126">System.Object</span></span>

## <span data-ttu-id="dfc57-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="dfc57-127">NOTES</span></span>

## <span data-ttu-id="dfc57-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dfc57-128">RELATED LINKS</span></span>


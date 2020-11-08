---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0fb6da4bde577d5a69c5bd85261822e3cf1865d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076903"
---
# <span data-ttu-id="7b49a-101">Get-AzsBlobService</span><span class="sxs-lookup"><span data-stu-id="7b49a-101">Get-AzsBlobService</span></span>

## <span data-ttu-id="7b49a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7b49a-102">SYNOPSIS</span></span>
<span data-ttu-id="7b49a-103">Возвращает службу больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="7b49a-103">Returns the blob service.</span></span>

## <span data-ttu-id="7b49a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7b49a-104">SYNTAX</span></span>

```
Get-AzsBlobService [-FarmName] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

## <span data-ttu-id="7b49a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b49a-105">DESCRIPTION</span></span>
<span data-ttu-id="7b49a-106">Возвращает службу больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="7b49a-106">Returns the blob service.</span></span>

## <span data-ttu-id="7b49a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7b49a-107">EXAMPLES</span></span>

### <span data-ttu-id="7b49a-108">ПРИМЕР 1</span><span class="sxs-lookup"><span data-stu-id="7b49a-108">EXAMPLE 1</span></span>
```
Get-AzsBlobService -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="7b49a-109">Скачайте службу больших двоичных объектов.</span><span class="sxs-lookup"><span data-stu-id="7b49a-109">Get the blob service.</span></span>

## <span data-ttu-id="7b49a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7b49a-110">PARAMETERS</span></span>

### <span data-ttu-id="7b49a-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="7b49a-111">-FarmName</span></span>
<span data-ttu-id="7b49a-112">Идентификатор фермы.</span><span class="sxs-lookup"><span data-stu-id="7b49a-112">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b49a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b49a-113">-ResourceGroupName</span></span>
<span data-ttu-id="7b49a-114">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7b49a-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b49a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b49a-115">CommonParameters</span></span>
<span data-ttu-id="7b49a-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7b49a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b49a-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b49a-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b49a-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7b49a-118">INPUTS</span></span>

## <span data-ttu-id="7b49a-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7b49a-119">OUTPUTS</span></span>

### <span data-ttu-id="7b49a-120">Microsoft. AzureStack. Management. Storage. admin. Models. BlobService</span><span class="sxs-lookup"><span data-stu-id="7b49a-120">Microsoft.AzureStack.Management.Storage.Admin.Models.BlobService</span></span>

## <span data-ttu-id="7b49a-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="7b49a-121">NOTES</span></span>

## <span data-ttu-id="7b49a-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7b49a-122">RELATED LINKS</span></span>
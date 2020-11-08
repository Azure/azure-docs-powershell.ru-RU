---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 20b70e2eeb1aa2d98f595dfe7bbe3075174c1f64
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94076850"
---
# <span data-ttu-id="29842-101">New-DirectoryTenantObject</span><span class="sxs-lookup"><span data-stu-id="29842-101">New-DirectoryTenantObject</span></span>

## <span data-ttu-id="29842-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29842-102">SYNOPSIS</span></span>
<span data-ttu-id="29842-103">Клиент службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="29842-103">Directory tenant.</span></span>

## <span data-ttu-id="29842-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29842-104">SYNTAX</span></span>

```
New-DirectoryTenantObject [[-Id] <String>] [[-Type] <String>]
 [[-Tags] <System.Collections.Generic.Dictionary`2[System.String,System.String]>] [[-Name] <String>]
 [[-TenantId] <String>] [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="29842-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29842-105">DESCRIPTION</span></span>
<span data-ttu-id="29842-106">Клиент службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="29842-106">Directory tenant.</span></span>

## <span data-ttu-id="29842-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29842-107">EXAMPLES</span></span>

### <span data-ttu-id="29842-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="29842-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="29842-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="29842-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="29842-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29842-110">PARAMETERS</span></span>

### <span data-ttu-id="29842-111">-ID</span><span class="sxs-lookup"><span data-stu-id="29842-111">-Id</span></span>
<span data-ttu-id="29842-112">URI ресурса.</span><span class="sxs-lookup"><span data-stu-id="29842-112">URI of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29842-113">-Location</span><span class="sxs-lookup"><span data-stu-id="29842-113">-Location</span></span>
<span data-ttu-id="29842-114">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="29842-114">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29842-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="29842-115">-Name</span></span>
<span data-ttu-id="29842-116">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="29842-116">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29842-117">-Теги</span><span class="sxs-lookup"><span data-stu-id="29842-117">-Tags</span></span>
<span data-ttu-id="29842-118">Список пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="29842-118">List of key-value pairs.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29842-119">-TenantId</span><span class="sxs-lookup"><span data-stu-id="29842-119">-TenantId</span></span>
<span data-ttu-id="29842-120">Уникальный идентификатор клиента.</span><span class="sxs-lookup"><span data-stu-id="29842-120">Tenant unique identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29842-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="29842-121">-Type</span></span>
<span data-ttu-id="29842-122">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="29842-122">Type of resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29842-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29842-123">CommonParameters</span></span>
<span data-ttu-id="29842-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29842-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29842-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29842-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29842-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29842-126">INPUTS</span></span>

## <span data-ttu-id="29842-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29842-127">OUTPUTS</span></span>

## <span data-ttu-id="29842-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="29842-128">NOTES</span></span>

## <span data-ttu-id="29842-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29842-129">RELATED LINKS</span></span>

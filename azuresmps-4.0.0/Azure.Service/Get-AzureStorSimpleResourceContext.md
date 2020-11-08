---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7CB42968-8F6F-4D84-9AE2-1000F280BF3C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 586abbd5f203ce00f6faa7975d9e2adbd0c7940e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076549"
---
# <span data-ttu-id="1c551-101">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="1c551-101">Get-AzureStorSimpleResourceContext</span></span>

## <span data-ttu-id="1c551-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c551-102">SYNOPSIS</span></span>
<span data-ttu-id="1c551-103">Возвращает текущий контекст ресурса.</span><span class="sxs-lookup"><span data-stu-id="1c551-103">Gets the current resource context.</span></span>

## <span data-ttu-id="1c551-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c551-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResourceContext [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1c551-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c551-105">DESCRIPTION</span></span>
<span data-ttu-id="1c551-106">Командлет **Get-AzureStorSimpleResourceContext** получает текущий контекст ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c551-106">The **Get-AzureStorSimpleResourceContext** cmdlet gets the current resource context.</span></span>

## <span data-ttu-id="1c551-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c551-107">EXAMPLES</span></span>

### <span data-ttu-id="1c551-108">Пример 1: получение текущего контекста</span><span class="sxs-lookup"><span data-stu-id="1c551-108">Example 1: Get the current context</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa" 
PS C:\> Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso63-Tsqa
```

<span data-ttu-id="1c551-109">Первая команда задает текущий контекст как ресурс с именем Contoso63-Tsqa с помощью командлета **SELECT-AzureStorSimpleResource** .</span><span class="sxs-lookup"><span data-stu-id="1c551-109">The first command sets the current context to be the resource named Contoso63-Tsqa by using the **Select-AzureStorSimpleResource** cmdlet.</span></span>

<span data-ttu-id="1c551-110">Вторая команда возвращает текущий контекст ресурса.</span><span class="sxs-lookup"><span data-stu-id="1c551-110">The second command gets the current resource context.</span></span>

### <span data-ttu-id="1c551-111">Пример 2. попытка получить текущий контекст</span><span class="sxs-lookup"><span data-stu-id="1c551-111">Example 2: Attempt to get the current context</span></span>
```
PS C:\>Get-AzureStorSimpleResourceContext
Get-AzureStorSimpleResourceContext : Resource Context is not set for your subscription. Please use
Select-AzureStorSimpleResource -ResourceName <<name>> to set
```

<span data-ttu-id="1c551-112">Эта команда возвращает текущий контекст.</span><span class="sxs-lookup"><span data-stu-id="1c551-112">This command gets the current context.</span></span>
<span data-ttu-id="1c551-113">В этом примере контекст не установлен.</span><span class="sxs-lookup"><span data-stu-id="1c551-113">In this example, no context has been set.</span></span>
<span data-ttu-id="1c551-114">Команда возвращает сообщение с описанием проблемы.</span><span class="sxs-lookup"><span data-stu-id="1c551-114">The command returns a message that explains the problem.</span></span>

## <span data-ttu-id="1c551-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c551-115">PARAMETERS</span></span>

### <span data-ttu-id="1c551-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="1c551-116">-Profile</span></span>
<span data-ttu-id="1c551-117">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="1c551-117">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c551-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c551-118">CommonParameters</span></span>
<span data-ttu-id="1c551-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c551-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c551-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c551-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c551-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c551-121">INPUTS</span></span>

### <span data-ttu-id="1c551-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="1c551-122">None</span></span>

## <span data-ttu-id="1c551-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c551-123">OUTPUTS</span></span>

### <span data-ttu-id="1c551-124">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="1c551-124">StorSimpleResourceContext</span></span>
<span data-ttu-id="1c551-125">Этот командлет возвращает объект **разделе ResourceContext** .</span><span class="sxs-lookup"><span data-stu-id="1c551-125">This cmdlet returns a **ResourceContext** object.</span></span>

## <span data-ttu-id="1c551-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c551-126">NOTES</span></span>

## <span data-ttu-id="1c551-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c551-127">RELATED LINKS</span></span>

[<span data-ttu-id="1c551-128">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="1c551-128">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="1c551-129">SELECT-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="1c551-129">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)



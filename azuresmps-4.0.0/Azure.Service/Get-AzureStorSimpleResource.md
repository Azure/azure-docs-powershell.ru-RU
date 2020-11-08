---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 482E8CD6-C38F-4BD5-8214-016D0D8C7FD0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6381b8e0fac5ebf047122f131af6087d5bb5a9fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075554"
---
# <span data-ttu-id="c15d1-101">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="c15d1-101">Get-AzureStorSimpleResource</span></span>

## <span data-ttu-id="c15d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c15d1-102">SYNOPSIS</span></span>
<span data-ttu-id="c15d1-103">Возвращает все созданные вами ресурсы.</span><span class="sxs-lookup"><span data-stu-id="c15d1-103">Gets all resources that you created.</span></span>

## <span data-ttu-id="c15d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c15d1-104">SYNTAX</span></span>

```
Get-AzureStorSimpleResource [-ResourceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c15d1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c15d1-105">DESCRIPTION</span></span>
<span data-ttu-id="c15d1-106">Командлет **Get-AzureStorSimpleResource** получает все ресурсы, созданные с помощью портала Azure.</span><span class="sxs-lookup"><span data-stu-id="c15d1-106">The **Get-AzureStorSimpleResource** cmdlet gets all resources that you created by using Azure Portal.</span></span>
<span data-ttu-id="c15d1-107">Командлет получает сведения, которые можно использовать для подключения к ресурсам.</span><span class="sxs-lookup"><span data-stu-id="c15d1-107">The cmdlet gets details you can use to connect to the resources.</span></span>

## <span data-ttu-id="c15d1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c15d1-108">EXAMPLES</span></span>

### <span data-ttu-id="c15d1-109">Пример 1: получение всех ресурсов</span><span class="sxs-lookup"><span data-stu-id="c15d1-109">Example 1: Get all resources</span></span>
```
PS C:\>Get-AzureStorSimpleResource
VERBOSE: ClientRequestId: 5cd61b91-ef40-43b4-986d-156e06d2ed65_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    8838459798595306468  Started
Contoso68-Tsqa                                    2859070203638134681  Started
Contoso73-Tsqa                                    7871392677286863733  Started
Contoso87-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 4 StorSimple resources.
```

<span data-ttu-id="c15d1-110">Эта команда получает все созданные вами ресурсы.</span><span class="sxs-lookup"><span data-stu-id="c15d1-110">This command gets all the resources you created.</span></span>
<span data-ttu-id="c15d1-111">В этом примере есть три ресурса.</span><span class="sxs-lookup"><span data-stu-id="c15d1-111">In this example, there are three resources.</span></span>

### <span data-ttu-id="c15d1-112">Пример 2: получение ресурса с помощью его имени</span><span class="sxs-lookup"><span data-stu-id="c15d1-112">Example 2: Get a resource by using its name</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso63-Tsqa"
VERBOSE: ClientRequestId: efc3c85c-12aa-4345-b6eb-ccc532de4825_PS

ResourceName                                      ResourceId           ResourceState
------------                                      ----------           -------------
Contoso63-Tsqa                                    1909806764156522689  Started
VERBOSE: Found 1 StorSimple resource.
```

<span data-ttu-id="c15d1-113">Эта команда возвращает ресурс с именем Contoso63-Tsqa.</span><span class="sxs-lookup"><span data-stu-id="c15d1-113">This command gets the resource named Contoso63-Tsqa.</span></span>

### <span data-ttu-id="c15d1-114">Пример 3: попытка получить несуществующий ресурс</span><span class="sxs-lookup"><span data-stu-id="c15d1-114">Example 3: Attempt to get a nonexistent resource</span></span>
```
PS C:\>Get-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
VERBOSE: ClientRequestId: 5d08d40b-f9d7-4d43-956f-13f01e89625b_PS
VERBOSE: Invalid input : Could not find a resource named Contoso64-Tsqa in your subscription.
```

<span data-ttu-id="c15d1-115">Эта команда пытается получить ресурс с именем Contoso64-Tsqa.</span><span class="sxs-lookup"><span data-stu-id="c15d1-115">This command attempts to get the resource named Contoso64-Tsqa.</span></span>
<span data-ttu-id="c15d1-116">Ресурс с таким именем отсутствует.</span><span class="sxs-lookup"><span data-stu-id="c15d1-116">There is no resource that has this name.</span></span>
<span data-ttu-id="c15d1-117">В этом примере не возвращается ни один ресурс.</span><span class="sxs-lookup"><span data-stu-id="c15d1-117">This example does not return any resource.</span></span>

## <span data-ttu-id="c15d1-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c15d1-118">PARAMETERS</span></span>

### <span data-ttu-id="c15d1-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="c15d1-119">-Profile</span></span>
<span data-ttu-id="c15d1-120">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="c15d1-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="c15d1-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c15d1-121">-ResourceName</span></span>
<span data-ttu-id="c15d1-122">Указывает имя ресурса, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="c15d1-122">Specifies the name of the resource that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c15d1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c15d1-123">CommonParameters</span></span>
<span data-ttu-id="c15d1-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c15d1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c15d1-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c15d1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c15d1-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c15d1-126">INPUTS</span></span>

### <span data-ttu-id="c15d1-127">Ничего</span><span class="sxs-lookup"><span data-stu-id="c15d1-127">None</span></span>

## <span data-ttu-id="c15d1-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c15d1-128">OUTPUTS</span></span>

### <span data-ttu-id="c15d1-129">IEnumerable \<ResourceCredentials\> , ResourceCredentials</span><span class="sxs-lookup"><span data-stu-id="c15d1-129">IEnumerable\<ResourceCredentials\>, ResourceCredentials</span></span>
<span data-ttu-id="c15d1-130">Этот командлет возвращает **ResourceCredentials** объекты, которые содержат следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="c15d1-130">This cmdlet returns **ResourceCredentials** objects that contain the following properties:</span></span> 

- <span data-ttu-id="c15d1-131">**ResourceName**</span><span class="sxs-lookup"><span data-stu-id="c15d1-131">**ResourceName**</span></span>
- <span data-ttu-id="c15d1-132">**ResouceId**</span><span class="sxs-lookup"><span data-stu-id="c15d1-132">**ResouceId**</span></span>
- <span data-ttu-id="c15d1-133">**ResourceState**</span><span class="sxs-lookup"><span data-stu-id="c15d1-133">**ResourceState**</span></span>

## <span data-ttu-id="c15d1-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c15d1-134">NOTES</span></span>

## <span data-ttu-id="c15d1-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c15d1-135">RELATED LINKS</span></span>

[<span data-ttu-id="c15d1-136">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="c15d1-136">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)

[<span data-ttu-id="c15d1-137">SELECT-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="c15d1-137">Select-AzureStorSimpleResource</span></span>](./Select-AzureStorSimpleResource.md)



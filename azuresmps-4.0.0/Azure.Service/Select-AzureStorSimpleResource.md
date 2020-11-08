---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075448"
---
# <span data-ttu-id="56f5f-101">Select-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="56f5f-101">Select-AzureStorSimpleResource</span></span>

## <span data-ttu-id="56f5f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="56f5f-103">Задает ресурс как текущий ресурс.</span><span class="sxs-lookup"><span data-stu-id="56f5f-103">Sets a resource as the current resource.</span></span>

## <span data-ttu-id="56f5f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56f5f-104">SYNTAX</span></span>

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="56f5f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56f5f-105">DESCRIPTION</span></span>
<span data-ttu-id="56f5f-106">Командлет **SELECT-AzureStorSimpleResource** задает ресурс как текущий ресурс.</span><span class="sxs-lookup"><span data-stu-id="56f5f-106">The **Select-AzureStorSimpleResource** cmdlet sets a resource as the current resource.</span></span>
<span data-ttu-id="56f5f-107">После выбора ресурса другие командлеты применяются к нему в этом контексте ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56f5f-107">After you select a resource, other cmdlets apply within that resource context.</span></span>

## <span data-ttu-id="56f5f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56f5f-108">EXAMPLES</span></span>

### <span data-ttu-id="56f5f-109">Пример 1: Выбор ресурса в первый раз</span><span class="sxs-lookup"><span data-stu-id="56f5f-109">Example 1: Select a resource for the first time</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="56f5f-110">Эта команда выбирает ресурс с именем "Contoso64-Tsqa" в качестве текущего контекста.</span><span class="sxs-lookup"><span data-stu-id="56f5f-110">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="56f5f-111">В этом примере на компьютере не был инициализирован этот контекст ранее и, следовательно, необходимо указать значение для параметра *RegistrationKey* .</span><span class="sxs-lookup"><span data-stu-id="56f5f-111">In this example, the computer has not had this context initialized previously, and, therefore, you must specify a value for the *RegistrationKey* parameter.</span></span>

### <span data-ttu-id="56f5f-112">Пример 2. попытка выбрать ресурс</span><span class="sxs-lookup"><span data-stu-id="56f5f-112">Example 2: Attempt to select a resource</span></span>
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### <span data-ttu-id="56f5f-113">Пример 3: выбор ранее выбранного ресурса</span><span class="sxs-lookup"><span data-stu-id="56f5f-113">Example 3: Select a previously selected resource</span></span>
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

<span data-ttu-id="56f5f-114">Эта команда выбирает ресурс с именем "Contoso64-Tsqa" в качестве текущего контекста.</span><span class="sxs-lookup"><span data-stu-id="56f5f-114">This command selects the resource named Contoso64-Tsqa as the current context.</span></span>
<span data-ttu-id="56f5f-115">В этом примере этот контекст был выбран ранее и, следовательно, вам не нужно указывать значение для параметра *RegistrationKey* .</span><span class="sxs-lookup"><span data-stu-id="56f5f-115">In this example, that context has previously been selected, and, therefore, you do not need to specify a value for the *RegistrationKey* parameter.</span></span>

## <span data-ttu-id="56f5f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56f5f-116">PARAMETERS</span></span>

### <span data-ttu-id="56f5f-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="56f5f-117">-Profile</span></span>
<span data-ttu-id="56f5f-118">Указывает профиль Azure.</span><span class="sxs-lookup"><span data-stu-id="56f5f-118">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="56f5f-119">-RegistrationKey</span><span class="sxs-lookup"><span data-stu-id="56f5f-119">-RegistrationKey</span></span>
<span data-ttu-id="56f5f-120">Указывает регистрационный ключ.</span><span class="sxs-lookup"><span data-stu-id="56f5f-120">Specifies a registration key.</span></span>
<span data-ttu-id="56f5f-121">Указание ключа при первом выборе ресурса.</span><span class="sxs-lookup"><span data-stu-id="56f5f-121">Specify a key the first time that you select a resource.</span></span>
<span data-ttu-id="56f5f-122">После того как этот командлет выберет текущий ресурс, командлеты применяют этот ключ, как требуется.</span><span class="sxs-lookup"><span data-stu-id="56f5f-122">After this cmdlet selects the current resource, cmdlets use this key, as required.</span></span>
<span data-ttu-id="56f5f-123">Дополнительные сведения можно найти в разделе [получение регистрационного ключа службы](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  ( https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) в сети разработчика Microsoft).</span><span class="sxs-lookup"><span data-stu-id="56f5f-123">For more information, see [Get the service registration key](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  (https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) on the Microsoft Developer Network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56f5f-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="56f5f-124">-ResourceName</span></span>
<span data-ttu-id="56f5f-125">Указывает имя ресурса для выбора в качестве текущего ресурса.</span><span class="sxs-lookup"><span data-stu-id="56f5f-125">Specifies the name of the resource to select as the current resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56f5f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f5f-126">CommonParameters</span></span>
<span data-ttu-id="56f5f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56f5f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f5f-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56f5f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f5f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56f5f-129">INPUTS</span></span>

### <span data-ttu-id="56f5f-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="56f5f-130">None</span></span>

## <span data-ttu-id="56f5f-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56f5f-131">OUTPUTS</span></span>

### <span data-ttu-id="56f5f-132">StorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="56f5f-132">StorSimpleResourceContext</span></span>
<span data-ttu-id="56f5f-133">Этот командлет возвращает объект **StorSimpleResourceContext** , содержащий сведения о контексте ресурса.</span><span class="sxs-lookup"><span data-stu-id="56f5f-133">This cmdlet returns a **StorSimpleResourceContext** object that contains details for the resource context.</span></span>

## <span data-ttu-id="56f5f-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="56f5f-134">NOTES</span></span>

## <span data-ttu-id="56f5f-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56f5f-135">RELATED LINKS</span></span>

[<span data-ttu-id="56f5f-136">Get-AzureStorSimpleResource</span><span class="sxs-lookup"><span data-stu-id="56f5f-136">Get-AzureStorSimpleResource</span></span>](./Get-AzureStorSimpleResource.md)

[<span data-ttu-id="56f5f-137">Get-AzureStorSimpleResourceContext</span><span class="sxs-lookup"><span data-stu-id="56f5f-137">Get-AzureStorSimpleResourceContext</span></span>](./Get-AzureStorSimpleResourceContext.md)



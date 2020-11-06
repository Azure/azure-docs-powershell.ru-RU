---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: d3251e0fabb99a9f16a497a445fa010a01187108
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93555788"
---
# <span data-ttu-id="0efac-101">Select-AzureRmProfile</span><span class="sxs-lookup"><span data-stu-id="0efac-101">Select-AzureRmProfile</span></span>

## <span data-ttu-id="0efac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0efac-102">SYNOPSIS</span></span>
<span data-ttu-id="0efac-103">Загрузка данных проверки подлинности Azure из файла.</span><span class="sxs-lookup"><span data-stu-id="0efac-103">Loads Azure authentication information from a file.</span></span>

## <span data-ttu-id="0efac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0efac-104">SYNTAX</span></span>

### <span data-ttu-id="0efac-105">InMemoryProfile</span><span class="sxs-lookup"><span data-stu-id="0efac-105">InMemoryProfile</span></span>
```
Select-AzureRmProfile [-Profile] <AzureRMProfile> [<CommonParameters>]
```

### <span data-ttu-id="0efac-106">ProfileFromDisk</span><span class="sxs-lookup"><span data-stu-id="0efac-106">ProfileFromDisk</span></span>
```
Select-AzureRmProfile [-Path] <String> [<CommonParameters>]
```

## <span data-ttu-id="0efac-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0efac-107">DESCRIPTION</span></span>
<span data-ttu-id="0efac-108">Командлет Select-AzureRmProfile загружает данные для проверки подлинности из файла, чтобы установить среду и контекст Azure.</span><span class="sxs-lookup"><span data-stu-id="0efac-108">The Select-AzureRmProfile cmdlet loads authentication information from a file to set the Azure environment and context.</span></span>
<span data-ttu-id="0efac-109">Командлеты, выполняемые в текущем сеансе, используют эти сведения для проверки подлинности запросов в диспетчере ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="0efac-109">Cmdlets that you run in the current session use this information to authenticate requests to Azure Resource Manager.</span></span>

## <span data-ttu-id="0efac-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0efac-110">EXAMPLES</span></span>

### <span data-ttu-id="0efac-111">Пример 1: Выбор профиля из PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="0efac-111">Example 1: Selecting a profile from a PSAzureProfile</span></span>
```
PS C:\> Select-AzureRmProfile -Profile (Add-AzureRmAccount)

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="0efac-112">В этом примере выполняется выбор профиля из PSAzureProfile, который передается в командлет.</span><span class="sxs-lookup"><span data-stu-id="0efac-112">This example selects a profile from a PSAzureProfile that is passed through to the cmdlet.</span></span>

### <span data-ttu-id="0efac-113">Пример 2: Выбор профиля из JSON-файла</span><span class="sxs-lookup"><span data-stu-id="0efac-113">Example 2: Selecting a profile from a JSON file</span></span>
```
PS C:\> Select-AzureRmProfile -Path C:\test.json

Environment           : AzureCloud
Account               : test@outlook.com
TenantId              : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SubscriptionId        : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
SubscriptionName      : Test Subscription
CurrentStorageAccount :
```

<span data-ttu-id="0efac-114">В этом примере выбирается профиль из JSON-файла, который передается в командлет.</span><span class="sxs-lookup"><span data-stu-id="0efac-114">This example selects a profile from a JSON file that is passed through to the cmdlet.</span></span> <span data-ttu-id="0efac-115">Этот JSON-файл можно создать из сохраняемого AzureRmProfile.</span><span class="sxs-lookup"><span data-stu-id="0efac-115">This JSON file can be created from Save-AzureRmProfile.</span></span>

## <span data-ttu-id="0efac-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0efac-116">PARAMETERS</span></span>

### <span data-ttu-id="0efac-117">-Path</span><span class="sxs-lookup"><span data-stu-id="0efac-117">-Path</span></span>
<span data-ttu-id="0efac-118">Задает путь к сведениям о профиле, сохраненным с помощью команды Save-AzureRMProfile.</span><span class="sxs-lookup"><span data-stu-id="0efac-118">Specifies the path to profile information saved by using Save-AzureRMProfile.</span></span>

```yaml
Type: String
Parameter Sets: ProfileFromDisk
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0efac-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="0efac-119">-Profile</span></span>
<span data-ttu-id="0efac-120">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0efac-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0efac-121">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0efac-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureRMProfile
Parameter Sets: InMemoryProfile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0efac-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0efac-122">CommonParameters</span></span>
<span data-ttu-id="0efac-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0efac-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0efac-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0efac-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0efac-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0efac-125">INPUTS</span></span>

## <span data-ttu-id="0efac-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0efac-126">OUTPUTS</span></span>

### <span data-ttu-id="0efac-127">PSAzureProfile</span><span class="sxs-lookup"><span data-stu-id="0efac-127">PSAzureProfile</span></span>

## <span data-ttu-id="0efac-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="0efac-128">NOTES</span></span>

## <span data-ttu-id="0efac-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0efac-129">RELATED LINKS</span></span>

[<span data-ttu-id="0efac-130">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="0efac-130">Get-AzureRMContext</span></span>]()


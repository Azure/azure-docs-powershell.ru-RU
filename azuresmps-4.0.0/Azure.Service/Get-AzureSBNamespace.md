---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1D433BD2-4604-474B-A2DA-BC80EE935E5C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ffbe5ae961c1733be68c902a9657b200cba0a5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075613"
---
# <span data-ttu-id="e0fce-101">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="e0fce-101">Get-AzureSBNamespace</span></span>

## <span data-ttu-id="e0fce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0fce-102">SYNOPSIS</span></span>
<span data-ttu-id="e0fce-103">Получает пространство имен.</span><span class="sxs-lookup"><span data-stu-id="e0fce-103">Gets the namespace.</span></span>


## <span data-ttu-id="e0fce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0fce-104">SYNTAX</span></span>

```
Get-AzureSBNamespace [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e0fce-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0fce-105">DESCRIPTION</span></span>
<span data-ttu-id="e0fce-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="e0fce-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e0fce-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e0fce-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e0fce-108">Командлет **Get-AzureSBNamespace** возвращает пространства имен служб служебной шины, связанные с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="e0fce-108">The **Get-AzureSBNamespace** cmdlet returns the Service Bus service namespaces associated with the current subscription.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="e0fce-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0fce-109">EXAMPLES</span></span>

### <span data-ttu-id="e0fce-110">Пример 1: получение пространства имен служебной шины</span><span class="sxs-lookup"><span data-stu-id="e0fce-110">Example 1: Get the Service Bus namespace</span></span>
```
PS C:\> Get-AzureSBNamespace
```

<span data-ttu-id="e0fce-111">В этом примере показано получение пространств имен служб служебной шины, связанных с текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="e0fce-111">This example gets the Service Bus service namespaces associated with the current subscription.</span></span>

## <span data-ttu-id="e0fce-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0fce-112">PARAMETERS</span></span>

### <span data-ttu-id="e0fce-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e0fce-113">-Name</span></span>
<span data-ttu-id="e0fce-114">Указывает имя пространства имен служебной шины для поиска.</span><span class="sxs-lookup"><span data-stu-id="e0fce-114">Specifies the name of a Service Bus namespace to look for.</span></span>

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

### <span data-ttu-id="e0fce-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="e0fce-115">-Profile</span></span>
<span data-ttu-id="e0fce-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="e0fce-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e0fce-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e0fce-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e0fce-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0fce-118">CommonParameters</span></span>
<span data-ttu-id="e0fce-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0fce-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0fce-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0fce-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0fce-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0fce-121">INPUTS</span></span>

## <span data-ttu-id="e0fce-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0fce-122">OUTPUTS</span></span>

## <span data-ttu-id="e0fce-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0fce-123">NOTES</span></span>

## <span data-ttu-id="e0fce-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0fce-124">RELATED LINKS</span></span>

[<span data-ttu-id="e0fce-125">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="e0fce-125">Get-AzureSBLocation</span></span>](./Get-AzureSBLocation.md)



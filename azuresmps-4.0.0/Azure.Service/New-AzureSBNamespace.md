---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0C806C0A-C199-4AF4-AE2A-11A2467A0873
online version: ''
schema: 2.0.0
ms.openlocfilehash: b11db019a3d7707ce93b2b2355efbaabe77fb91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075988"
---
# <span data-ttu-id="04b3e-101">New-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="04b3e-101">New-AzureSBNamespace</span></span>

## <span data-ttu-id="04b3e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="04b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="04b3e-103">Создание пространства имен.</span><span class="sxs-lookup"><span data-stu-id="04b3e-103">Creates a namespace.</span></span>

## <span data-ttu-id="04b3e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="04b3e-104">SYNTAX</span></span>

```
New-AzureSBNamespace -Name <String> [-Location <String>] [-CreateACSNamespace <Boolean>]
 -NamespaceType <NamespaceType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="04b3e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="04b3e-105">DESCRIPTION</span></span>
<span data-ttu-id="04b3e-106">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="04b3e-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="04b3e-107">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="04b3e-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="04b3e-108">Командлет **New-AzureSBNamespace** создает пространство имен службы для использования с шиной обслуживания в Azure.</span><span class="sxs-lookup"><span data-stu-id="04b3e-108">The **New-AzureSBNamespace** cmdlet creates a service namespace for use with Service Bus in Azure.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="04b3e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="04b3e-109">EXAMPLES</span></span>

### <span data-ttu-id="04b3e-110">Пример 1: создание пространства имен службы</span><span class="sxs-lookup"><span data-stu-id="04b3e-110">Example 1: Create a service namespace</span></span>
```
PS C:\> New-AzureSBNamespace -Name myNameSpace -Location East US 
PS C:\> New-AzureSBNamespace myNameSpace 'East US'
```

<span data-ttu-id="04b3e-111">В примерах создается пространство имен службы для использования с шиной обслуживания в Azure.</span><span class="sxs-lookup"><span data-stu-id="04b3e-111">The examples create a service namespace for use with Service Bus in Azure.</span></span>
<span data-ttu-id="04b3e-112">Оба примера содержат необходимые значения параметров, но только первые содержат имена параметров.</span><span class="sxs-lookup"><span data-stu-id="04b3e-112">Both examples include the required parameter values, but only the first includes the parameter names.</span></span>
<span data-ttu-id="04b3e-113">Второй пример можно использовать, так как оба параметра являются позиционными и их значения заданы в нужном порядке.</span><span class="sxs-lookup"><span data-stu-id="04b3e-113">The second example can be used because both parameters are positional and their values are given in the required order.</span></span>

## <span data-ttu-id="04b3e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="04b3e-114">PARAMETERS</span></span>

### <span data-ttu-id="04b3e-115">-CreateACSNamespace</span><span class="sxs-lookup"><span data-stu-id="04b3e-115">-CreateACSNamespace</span></span>
<span data-ttu-id="04b3e-116">Указывает, нужно ли создавать связанное пространство имен ACS в дополнение к пространству имен службы.</span><span class="sxs-lookup"><span data-stu-id="04b3e-116">Specifies whether to create an associated ACS namespace in addition to the service namespace.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04b3e-117">-Location</span><span class="sxs-lookup"><span data-stu-id="04b3e-117">-Location</span></span>
<span data-ttu-id="04b3e-118">Указывает регион для нового пространства имен.</span><span class="sxs-lookup"><span data-stu-id="04b3e-118">Specifies a region for the new namespace.</span></span>

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

### <span data-ttu-id="04b3e-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="04b3e-119">-Name</span></span>
<span data-ttu-id="04b3e-120">Задает имя нового пространства имен.</span><span class="sxs-lookup"><span data-stu-id="04b3e-120">Specifies a name for the new namespace.</span></span>

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

### <span data-ttu-id="04b3e-121">-NamespaceType</span><span class="sxs-lookup"><span data-stu-id="04b3e-121">-NamespaceType</span></span>
<span data-ttu-id="04b3e-122">Укажите, следует ли использовать пространство имен для концентраторов сообщений или уведомлений.</span><span class="sxs-lookup"><span data-stu-id="04b3e-122">Specify a whether to use the namespace for Messaging or Notification Hubs.</span></span>

```yaml
Type: NamespaceType
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04b3e-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="04b3e-123">-Profile</span></span>
<span data-ttu-id="04b3e-124">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="04b3e-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="04b3e-125">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="04b3e-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="04b3e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04b3e-126">CommonParameters</span></span>
<span data-ttu-id="04b3e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="04b3e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04b3e-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04b3e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04b3e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="04b3e-129">INPUTS</span></span>

## <span data-ttu-id="04b3e-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="04b3e-130">OUTPUTS</span></span>

## <span data-ttu-id="04b3e-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="04b3e-131">NOTES</span></span>

## <span data-ttu-id="04b3e-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="04b3e-132">RELATED LINKS</span></span>

[<span data-ttu-id="04b3e-133">Remove-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="04b3e-133">Remove-AzureSBNamespace</span></span>](./Remove-AzureSBNamespace.md)



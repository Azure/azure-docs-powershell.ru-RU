---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 6C4081EE-0BCD-4285-8ABB-778BD95BFE4F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37f6e5b1152af79b2fc199199bf2b872bfbfa4ec
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075911"
---
# <span data-ttu-id="100d5-101">New-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="100d5-101">New-AzureMediaServicesAccount</span></span>

## <span data-ttu-id="100d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="100d5-102">SYNOPSIS</span></span>
<span data-ttu-id="100d5-103">Создание учетной записи служб мультимедиа Azure.</span><span class="sxs-lookup"><span data-stu-id="100d5-103">Creates an Azure Media Services account.</span></span>

<span data-ttu-id="100d5-104">**Примечание.** Эта версия устарела, ознакомьтесь с [более новой версией](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span><span class="sxs-lookup"><span data-stu-id="100d5-104">**Note:** This version is deprecated, please see the [newer version](https://docs.microsoft.com/powershell/module/azurerm.media/?view=azurermps-5.4.0#media_services).</span></span>

## <span data-ttu-id="100d5-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="100d5-105">SYNTAX</span></span>

```
New-AzureMediaServicesAccount -Name <String> -Location <String> -StorageAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="100d5-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="100d5-106">DESCRIPTION</span></span>
<span data-ttu-id="100d5-107">В этом разделе описан командлет в версии 0.8.10 модуля Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="100d5-107">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="100d5-108">Чтобы получить версию модуля, который вы используете, введите в командной консоли Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="100d5-108">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="100d5-109">Командлет **New-AzureMediaServicesAccount** создает новую учетную запись служб мультимедиа с указанным именем учетной записи служб мультимедиа, расположением центра обработки данных, в котором вы хотите создать учетную запись, и именем существующей учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="100d5-109">The **New-AzureMediaServicesAccount** cmdlet creates a new Media Services account with the specified Media Services account name, datacenter location where you want to create the account, and an existing storage account name.</span></span>
<span data-ttu-id="100d5-110">Учетная запись хранения должна находиться в том же центре обработки данных, что и новая учетная запись служб мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="100d5-110">The storage account has to be located in the same data center as the new Media Services account.</span></span>

## <span data-ttu-id="100d5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="100d5-111">EXAMPLES</span></span>

### <span data-ttu-id="100d5-112">Пример 1: создание новой учетной записи служб мультимедиа</span><span class="sxs-lookup"><span data-stu-id="100d5-112">Example 1: Create a new Media Services account</span></span>
```
PS C:\> New-AzureMediaServicesAccount -Name "mediaserviceaccount" -StorageAccountName "storageaccount " -Location "West US"
```

## <span data-ttu-id="100d5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="100d5-113">PARAMETERS</span></span>

### <span data-ttu-id="100d5-114">-Location</span><span class="sxs-lookup"><span data-stu-id="100d5-114">-Location</span></span>
<span data-ttu-id="100d5-115">Указывает расположение центра обработки данных службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="100d5-115">Specifies the Media Services datacenter location.</span></span>

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

### <span data-ttu-id="100d5-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="100d5-116">-Name</span></span>
<span data-ttu-id="100d5-117">Указывает имя учетной записи служб мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="100d5-117">Specifies the Media Services account name.</span></span>

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

### <span data-ttu-id="100d5-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="100d5-118">-Profile</span></span>
<span data-ttu-id="100d5-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="100d5-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="100d5-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="100d5-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="100d5-121">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="100d5-121">-StorageAccountName</span></span>
<span data-ttu-id="100d5-122">Указывает имя учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="100d5-122">Specifies the storage account name.</span></span>
<span data-ttu-id="100d5-123">Учетная запись хранилища уже должна существовать в том же центре обработки данных, что и новая учетная запись служб мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="100d5-123">The storage account must already exist in the same datacenter as the new Media Services account.</span></span>

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

### <span data-ttu-id="100d5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="100d5-124">CommonParameters</span></span>
<span data-ttu-id="100d5-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="100d5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="100d5-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="100d5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="100d5-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="100d5-127">INPUTS</span></span>

## <span data-ttu-id="100d5-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="100d5-128">OUTPUTS</span></span>

## <span data-ttu-id="100d5-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="100d5-129">NOTES</span></span>

## <span data-ttu-id="100d5-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="100d5-130">RELATED LINKS</span></span>

[<span data-ttu-id="100d5-131">Использование Azure PowerShell для служб мультимедиа</span><span class="sxs-lookup"><span data-stu-id="100d5-131">How to use Azure PowerShell for Media Services</span></span>](https://go.microsoft.com/fwlink/?LinkId=324179)

[<span data-ttu-id="100d5-132">Get-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="100d5-132">Get-AzureMediaServicesAccount</span></span>](./Get-AzureMediaServicesAccount.md)

[<span data-ttu-id="100d5-133">Remove-AzureMediaServicesAccount</span><span class="sxs-lookup"><span data-stu-id="100d5-133">Remove-AzureMediaServicesAccount</span></span>](./Remove-AzureMediaServicesAccount.md)



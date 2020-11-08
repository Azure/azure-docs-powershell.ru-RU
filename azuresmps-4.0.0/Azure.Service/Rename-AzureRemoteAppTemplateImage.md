---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 22571840-C27C-4208-A755-EF89E6C4B604
online version: ''
schema: 2.0.0
ms.openlocfilehash: 61cfeab9e02968c7b03e694b9913d4cbe4b3c90a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075474"
---
# <span data-ttu-id="ef186-101">Rename-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ef186-101">Rename-AzureRemoteAppTemplateImage</span></span>

## <span data-ttu-id="ef186-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ef186-102">SYNOPSIS</span></span>
<span data-ttu-id="ef186-103">Переименовывает образ шаблона Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ef186-103">Renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="ef186-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ef186-104">SYNTAX</span></span>

```
Rename-AzureRemoteAppTemplateImage [-ImageName] <String> [-NewName] <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="ef186-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef186-105">DESCRIPTION</span></span>
<span data-ttu-id="ef186-106">Командлет **Rename-AzureRemoteAppTemplateImage** переименовывает образ шаблона Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ef186-106">The **Rename-AzureRemoteAppTemplateImage** cmdlet renames an Azure RemoteApp template image.</span></span>

## <span data-ttu-id="ef186-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ef186-107">EXAMPLES</span></span>

### <span data-ttu-id="ef186-108">Пример 1: Переименование изображения шаблона</span><span class="sxs-lookup"><span data-stu-id="ef186-108">Example 1: Rename a template image</span></span>
```
PS C:\> Rename-AzureRemoteAppTemplateImage -ImageName "ContosoApps" -NewName "ContosoFinanceApps"
```

<span data-ttu-id="ef186-109">Эта команда переименовывает образ шаблона Azure RemoteApp с именем ContosoApps в ContosoFinanceApps.</span><span class="sxs-lookup"><span data-stu-id="ef186-109">This command renames the Azure RemoteApp template image named ContosoApps to ContosoFinanceApps.</span></span>

## <span data-ttu-id="ef186-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ef186-110">PARAMETERS</span></span>

### <span data-ttu-id="ef186-111">-ImageName</span><span class="sxs-lookup"><span data-stu-id="ef186-111">-ImageName</span></span>
<span data-ttu-id="ef186-112">Указывает имя образа шаблона Azure RemoteApp для переименования.</span><span class="sxs-lookup"><span data-stu-id="ef186-112">Specifies the name of an Azure RemoteApp template image to rename.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef186-113">-NewName</span><span class="sxs-lookup"><span data-stu-id="ef186-113">-NewName</span></span>
<span data-ttu-id="ef186-114">Указывает новое имя для образа шаблона Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="ef186-114">Specifies a new name for an Azure RemoteApp template image.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef186-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="ef186-115">-Profile</span></span>
<span data-ttu-id="ef186-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ef186-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ef186-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef186-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ef186-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef186-118">CommonParameters</span></span>
<span data-ttu-id="ef186-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ef186-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef186-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef186-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef186-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ef186-121">INPUTS</span></span>

## <span data-ttu-id="ef186-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef186-122">OUTPUTS</span></span>

## <span data-ttu-id="ef186-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="ef186-123">NOTES</span></span>

## <span data-ttu-id="ef186-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef186-124">RELATED LINKS</span></span>

[<span data-ttu-id="ef186-125">Get-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ef186-125">Get-AzureRemoteAppTemplateImage</span></span>](./Get-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="ef186-126">New-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ef186-126">New-AzureRemoteAppTemplateImage</span></span>](./New-AzureRemoteAppTemplateImage.md)

[<span data-ttu-id="ef186-127">Remove-AzureRemoteAppTemplateImage</span><span class="sxs-lookup"><span data-stu-id="ef186-127">Remove-AzureRemoteAppTemplateImage</span></span>](./Remove-AzureRemoteAppTemplateImage.md)



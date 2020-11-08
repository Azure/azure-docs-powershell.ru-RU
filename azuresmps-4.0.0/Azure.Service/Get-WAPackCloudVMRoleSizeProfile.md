---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 453AEA42-E29C-4FF2-9210-0DD88B77DC07
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29c7f8bc814ddf5295064d89eeaf34c8e7274916
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076508"
---
# <span data-ttu-id="0aa9a-101">Get-WAPackCloudVMRoleSizeProfile</span><span class="sxs-lookup"><span data-stu-id="0aa9a-101">Get-WAPackCloudVMRoleSizeProfile</span></span>

## <span data-ttu-id="0aa9a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0aa9a-102">SYNOPSIS</span></span>
<span data-ttu-id="0aa9a-103">Возвращает объекты профиля размера роли облачной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0aa9a-103">Gets Cloud VM Role Size profile objects.</span></span>

## <span data-ttu-id="0aa9a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0aa9a-104">SYNTAX</span></span>

### <span data-ttu-id="0aa9a-105">Пустой (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0aa9a-105">Empty (Default)</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0aa9a-106">FromName</span><span class="sxs-lookup"><span data-stu-id="0aa9a-106">FromName</span></span>
```
Get-WAPackCloudVMRoleSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0aa9a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0aa9a-107">DESCRIPTION</span></span>
<span data-ttu-id="0aa9a-108">Командлет **Get-WAPackCloudVMRoleSizeProfile** получает объекты профиля размера роли облачной ВМ для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="0aa9a-108">The **Get-WAPackCloudVMRoleSizeProfile** cmdlet gets Cloud VM Role size profile objects for virtual machines.</span></span>

## <span data-ttu-id="0aa9a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0aa9a-109">EXAMPLES</span></span>

### <span data-ttu-id="0aa9a-110">Пример 1: получение профиля размера роли облачной ВМ с помощью имени</span><span class="sxs-lookup"><span data-stu-id="0aa9a-110">Example 1: Get a Cloud VM Role size profile by using a name</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile -Name "Small"
```

<span data-ttu-id="0aa9a-111">Эта команда получает профиль размера с именем Small.</span><span class="sxs-lookup"><span data-stu-id="0aa9a-111">This command gets the size profile named Small.</span></span>

### <span data-ttu-id="0aa9a-112">Пример 2: получение всех профилей размера роли виртуальной машины облака</span><span class="sxs-lookup"><span data-stu-id="0aa9a-112">Example 2: Get all Cloud VM Role size profiles</span></span>
```
PS C:\> Get-WAPackCloudVMRoleSizeProfile
```

<span data-ttu-id="0aa9a-113">Эта команда получает все профили размера.</span><span class="sxs-lookup"><span data-stu-id="0aa9a-113">This command gets all the size profiles.</span></span>

## <span data-ttu-id="0aa9a-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0aa9a-114">PARAMETERS</span></span>

### <span data-ttu-id="0aa9a-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0aa9a-115">-Name</span></span>
<span data-ttu-id="0aa9a-116">Указывает имя профиля размера роли облачной ВМ.</span><span class="sxs-lookup"><span data-stu-id="0aa9a-116">Specifies the name of a Cloud VM Role size profile.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aa9a-117">-Profile</span><span class="sxs-lookup"><span data-stu-id="0aa9a-117">-Profile</span></span>
<span data-ttu-id="0aa9a-118">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0aa9a-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0aa9a-119">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0aa9a-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0aa9a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aa9a-120">CommonParameters</span></span>
<span data-ttu-id="0aa9a-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0aa9a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aa9a-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aa9a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aa9a-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0aa9a-123">INPUTS</span></span>

## <span data-ttu-id="0aa9a-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0aa9a-124">OUTPUTS</span></span>

## <span data-ttu-id="0aa9a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="0aa9a-125">NOTES</span></span>

## <span data-ttu-id="0aa9a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0aa9a-126">RELATED LINKS</span></span>

[<span data-ttu-id="0aa9a-127">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="0aa9a-127">Get-WAPackVM</span></span>](./Get-WAPackVM.md)



---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: D61E0D1A-7A79-436C-BB1B-740E31BC982D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49aa46cf44d07e9063f819d6ba90788e0fb221fa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075910"
---
# <span data-ttu-id="014fa-101">New-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="014fa-101">New-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="014fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="014fa-102">SYNOPSIS</span></span>
<span data-ttu-id="014fa-103">Создание группы безопасности сети Azure.</span><span class="sxs-lookup"><span data-stu-id="014fa-103">Creates an Azure network security group.</span></span>

## <span data-ttu-id="014fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="014fa-104">SYNTAX</span></span>

```
New-AzureNetworkSecurityGroup -Name <String> -Location <String> [-Label <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="014fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="014fa-105">DESCRIPTION</span></span>
<span data-ttu-id="014fa-106">Командлет **New-AzureNetworkSecurityGroup** создает группу безопасности сети Azure в расположении.</span><span class="sxs-lookup"><span data-stu-id="014fa-106">The **New-AzureNetworkSecurityGroup** cmdlet creates an Azure network security group in a location.</span></span>

## <span data-ttu-id="014fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="014fa-107">EXAMPLES</span></span>

## <span data-ttu-id="014fa-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="014fa-108">PARAMETERS</span></span>

### <span data-ttu-id="014fa-109">-Label</span><span class="sxs-lookup"><span data-stu-id="014fa-109">-Label</span></span>
<span data-ttu-id="014fa-110">Задает описание новой группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="014fa-110">Specifies a description for the new network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014fa-111">-Location</span><span class="sxs-lookup"><span data-stu-id="014fa-111">-Location</span></span>
<span data-ttu-id="014fa-112">Указывает расположение Azure, в котором этот командлет создает сетевую группу безопасности.</span><span class="sxs-lookup"><span data-stu-id="014fa-112">Specifies the Azure location in which this cmdlet creates a network security group.</span></span>
<span data-ttu-id="014fa-113">Для получения допустимых местоположений используйте командлет Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="014fa-113">To obtain valid locations, use the Get-AzureLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014fa-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="014fa-114">-Name</span></span>
<span data-ttu-id="014fa-115">Задает имя для новой группы безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="014fa-115">Specifies a name for the new network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="014fa-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="014fa-116">-Profile</span></span>
<span data-ttu-id="014fa-117">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="014fa-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="014fa-118">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="014fa-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="014fa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="014fa-119">CommonParameters</span></span>
<span data-ttu-id="014fa-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="014fa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="014fa-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="014fa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="014fa-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="014fa-122">INPUTS</span></span>

## <span data-ttu-id="014fa-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="014fa-123">OUTPUTS</span></span>

## <span data-ttu-id="014fa-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="014fa-124">NOTES</span></span>

## <span data-ttu-id="014fa-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="014fa-125">RELATED LINKS</span></span>

[<span data-ttu-id="014fa-126">Get-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="014fa-126">Get-AzureNetworkSecurityGroup</span></span>](./Get-AzureNetworkSecurityGroup.md)



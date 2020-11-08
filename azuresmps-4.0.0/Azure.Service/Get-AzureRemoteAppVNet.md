---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076570"
---
# <span data-ttu-id="d5cca-101">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="d5cca-101">Get-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="d5cca-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5cca-102">SYNOPSIS</span></span>
<span data-ttu-id="d5cca-103">Получение сведений о виртуальных сетях RemoteApp Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="d5cca-103">Retrieves information about Azure RemoteApp virtual networks in Azure.</span></span>

## <span data-ttu-id="d5cca-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5cca-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5cca-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5cca-105">DESCRIPTION</span></span>
<span data-ttu-id="d5cca-106">Командлет **Get-AzureRemoteAppVNet** извлекает сведения о виртуальных сетях Azure RemoteApp в Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d5cca-106">The **Get-AzureRemoteAppVNet** cmdlet retrieves information about Azure RemoteApp virtual networks in Microsoft Azure.</span></span>
<span data-ttu-id="d5cca-107">Этот командлет возвращает объект, содержащий сведения об указанной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5cca-107">This cmdlet returns an object that contains information about a specified virtual network.</span></span>
<span data-ttu-id="d5cca-108">Если виртуальная сеть не указана, этот командлет возвращает сведения обо всех виртуальных сетях в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="d5cca-108">If no virtual network is specified, this cmdlet returns information about all the virtual networks in the current subscription.</span></span>

## <span data-ttu-id="d5cca-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5cca-109">EXAMPLES</span></span>

### <span data-ttu-id="d5cca-110">Пример 1: получение сведений о виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="d5cca-110">Example 1: Retrieve information about a virtual network</span></span>
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

<span data-ttu-id="d5cca-111">Эта команда получает сведения о виртуальной сети с именем ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="d5cca-111">This command gets information about the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="d5cca-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5cca-112">PARAMETERS</span></span>

### <span data-ttu-id="d5cca-113">-IncludeSharedKey</span><span class="sxs-lookup"><span data-stu-id="d5cca-113">-IncludeSharedKey</span></span>
<span data-ttu-id="d5cca-114">Указывает на то, что этот командлет включает значение общего ключа в извлеченных данных о виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="d5cca-114">Indicates that this cmdlet includes the shared key value in the information it retrieves about the virtual network.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5cca-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="d5cca-115">-Profile</span></span>
<span data-ttu-id="d5cca-116">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d5cca-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d5cca-117">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d5cca-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d5cca-118">-VNetName</span><span class="sxs-lookup"><span data-stu-id="d5cca-118">-VNetName</span></span>
<span data-ttu-id="d5cca-119">Указывает имя виртуальной сети RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="d5cca-119">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="d5cca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5cca-120">CommonParameters</span></span>
<span data-ttu-id="d5cca-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5cca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5cca-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5cca-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5cca-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5cca-123">INPUTS</span></span>

## <span data-ttu-id="d5cca-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5cca-124">OUTPUTS</span></span>

## <span data-ttu-id="d5cca-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5cca-125">NOTES</span></span>

## <span data-ttu-id="d5cca-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5cca-126">RELATED LINKS</span></span>

[<span data-ttu-id="d5cca-127">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="d5cca-127">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)



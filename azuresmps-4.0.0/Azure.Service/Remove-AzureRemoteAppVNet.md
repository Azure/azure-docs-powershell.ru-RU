---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 000B2335-E374-47CC-8165-40AE807C090F
online version: ''
schema: 2.0.0
ms.openlocfilehash: c097884326d1430804f1d577629b62041bfd402b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076146"
---
# <span data-ttu-id="242c2-101">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="242c2-101">Remove-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="242c2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="242c2-102">SYNOPSIS</span></span>
<span data-ttu-id="242c2-103">Удаляет виртуальную сеть RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="242c2-103">Deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="242c2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="242c2-104">SYNTAX</span></span>

```
Remove-AzureRemoteAppVNet -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="242c2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="242c2-105">DESCRIPTION</span></span>
<span data-ttu-id="242c2-106">Командлет **Remove-AzureRemoteAppVNet** удаляет виртуальную сеть RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="242c2-106">The **Remove-AzureRemoteAppVNet** cmdlet deletes an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="242c2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="242c2-107">EXAMPLES</span></span>

### <span data-ttu-id="242c2-108">Пример 1: удаление указанной виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="242c2-108">Example 1: Delete a specified virtual network</span></span>
```
PS C:\> Remove-AzureRemoteAppVnet -VNetName "ContosoVNet"
```

<span data-ttu-id="242c2-109">Эта команда удаляет виртуальную сеть с именем ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="242c2-109">This command deletes the virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="242c2-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="242c2-110">PARAMETERS</span></span>

### <span data-ttu-id="242c2-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="242c2-111">-Profile</span></span>
<span data-ttu-id="242c2-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="242c2-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="242c2-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="242c2-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="242c2-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="242c2-114">-VNetName</span></span>
<span data-ttu-id="242c2-115">Указывает имя виртуальной сети RemoteApp Azure, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="242c2-115">Specifies the name of the Azure RemoteApp virtual network to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="242c2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="242c2-116">CommonParameters</span></span>
<span data-ttu-id="242c2-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="242c2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="242c2-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="242c2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="242c2-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="242c2-119">INPUTS</span></span>

## <span data-ttu-id="242c2-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="242c2-120">OUTPUTS</span></span>

## <span data-ttu-id="242c2-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="242c2-121">NOTES</span></span>

## <span data-ttu-id="242c2-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="242c2-122">RELATED LINKS</span></span>

[<span data-ttu-id="242c2-123">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="242c2-123">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="242c2-124">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="242c2-124">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)



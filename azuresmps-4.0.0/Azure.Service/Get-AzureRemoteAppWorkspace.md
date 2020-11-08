---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 035B294E-6A1B-41E9-ACFF-D66F9C1A0B11
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9218862bb1e61abe548a94ed5297a6ce69237d54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075619"
---
# <span data-ttu-id="484b6-101">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="484b6-101">Get-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="484b6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="484b6-102">SYNOPSIS</span></span>
<span data-ttu-id="484b6-103">Получение сведений о рабочей области Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="484b6-103">Retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="484b6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="484b6-104">SYNTAX</span></span>

```
Get-AzureRemoteAppWorkspace [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="484b6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="484b6-105">DESCRIPTION</span></span>
<span data-ttu-id="484b6-106">Командлет **Get-AzureRemoteAppWorkspace** извлекает сведения о рабочей области Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="484b6-106">The **Get-AzureRemoteAppWorkspace** cmdlet retrieves information about an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="484b6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="484b6-107">EXAMPLES</span></span>

### <span data-ttu-id="484b6-108">Пример 1: получение сведений о рабочей области</span><span class="sxs-lookup"><span data-stu-id="484b6-108">Example 1: Retrieve information about a workspace</span></span>
```
PS C:\> Get-AzureRemoteAppWorkspace
ClientUrl                               EndUserFeedName
---------                               ---------------
https://www.remoteapp.windowsazure.com/ Contoso Work Applications
```

<span data-ttu-id="484b6-109">Эта команда извлекает сведения о рабочей области Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="484b6-109">This command retrieves information about the Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="484b6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="484b6-110">PARAMETERS</span></span>

### <span data-ttu-id="484b6-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="484b6-111">-Profile</span></span>
<span data-ttu-id="484b6-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="484b6-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="484b6-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="484b6-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="484b6-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="484b6-114">CommonParameters</span></span>
<span data-ttu-id="484b6-115">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="484b6-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="484b6-116">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="484b6-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="484b6-117">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="484b6-117">INPUTS</span></span>

## <span data-ttu-id="484b6-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="484b6-118">OUTPUTS</span></span>

## <span data-ttu-id="484b6-119">Пуск</span><span class="sxs-lookup"><span data-stu-id="484b6-119">NOTES</span></span>

## <span data-ttu-id="484b6-120">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="484b6-120">RELATED LINKS</span></span>

[<span data-ttu-id="484b6-121">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="484b6-121">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)



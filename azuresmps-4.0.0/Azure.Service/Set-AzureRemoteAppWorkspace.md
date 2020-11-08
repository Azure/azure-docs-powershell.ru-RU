---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 608B4B5E-5DB2-4291-966C-0B25F8D4FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 18c5f50a2804aeca545c44a5c0728bf7003e9d8e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076051"
---
# <span data-ttu-id="2b79d-101">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="2b79d-101">Set-AzureRemoteAppWorkspace</span></span>

## <span data-ttu-id="2b79d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b79d-102">SYNOPSIS</span></span>
<span data-ttu-id="2b79d-103">Задает свойства рабочей области RemoteApp для Azure.</span><span class="sxs-lookup"><span data-stu-id="2b79d-103">Sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="2b79d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b79d-104">SYNTAX</span></span>

```
Set-AzureRemoteAppWorkspace [-WorkspaceName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2b79d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b79d-105">DESCRIPTION</span></span>
<span data-ttu-id="2b79d-106">Командлет **Set-AzureRemoteAppWorkspace** задает свойства рабочей области RemoteApp для Azure.</span><span class="sxs-lookup"><span data-stu-id="2b79d-106">The **Set-AzureRemoteAppWorkspace** cmdlet sets the properties of an Azure RemoteApp workspace.</span></span>

## <span data-ttu-id="2b79d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b79d-107">EXAMPLES</span></span>

### <span data-ttu-id="2b79d-108">Пример 1: Настройка имени рабочей области</span><span class="sxs-lookup"><span data-stu-id="2b79d-108">Example 1: Set the workspace name</span></span>
```
PS C:\> Set-AzureRemoteAppWorkspace -WorkspaceName "Contoso Work Applications"

TrackingId
----------
12345
```

<span data-ttu-id="2b79d-109">Эта команда задает имя рабочей области RemoteApp для Azure рабочими приложениями contoso.</span><span class="sxs-lookup"><span data-stu-id="2b79d-109">This command sets the Azure RemoteApp workspace name to Contoso Work Applications.</span></span>

## <span data-ttu-id="2b79d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b79d-110">PARAMETERS</span></span>

### <span data-ttu-id="2b79d-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="2b79d-111">-Profile</span></span>
<span data-ttu-id="2b79d-112">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2b79d-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2b79d-113">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2b79d-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2b79d-114">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2b79d-114">-WorkspaceName</span></span>
<span data-ttu-id="2b79d-115">Указывает имя рабочей области Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="2b79d-115">Specifies the name of the Azure RemoteApp workspace.</span></span>

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

### <span data-ttu-id="2b79d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b79d-116">CommonParameters</span></span>
<span data-ttu-id="2b79d-117">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b79d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b79d-118">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b79d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b79d-119">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b79d-119">INPUTS</span></span>

## <span data-ttu-id="2b79d-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b79d-120">OUTPUTS</span></span>

## <span data-ttu-id="2b79d-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b79d-121">NOTES</span></span>
* <span data-ttu-id="2b79d-122">Все коллекции Azure RemoteApp для указанной подписки находятся в общей рабочей области.</span><span class="sxs-lookup"><span data-stu-id="2b79d-122">All Azure RemoteApp collections for a specified subscription exist within a shared workspace.</span></span>

## <span data-ttu-id="2b79d-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b79d-123">RELATED LINKS</span></span>

[<span data-ttu-id="2b79d-124">Get-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="2b79d-124">Get-AzureRemoteAppWorkspace</span></span>](./Get-AzureRemoteAppWorkspace.md)



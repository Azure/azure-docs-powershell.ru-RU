---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 4136A0EF-2682-4B17-BC37-53CD43F5940B
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b884da0395313ddc8aa4d0e301b37849ec3d57
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94076322"
---
# <span data-ttu-id="d3af6-101">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="d3af6-101">Get-AzureRemoteAppOperationResult</span></span>

## <span data-ttu-id="d3af6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d3af6-102">SYNOPSIS</span></span>
<span data-ttu-id="d3af6-103">Получение результата операции Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d3af6-103">Retrieves the result of an Azure RemoteApp operation.</span></span>

## <span data-ttu-id="d3af6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d3af6-104">SYNTAX</span></span>

```
Get-AzureRemoteAppOperationResult [-TrackingId] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d3af6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3af6-105">DESCRIPTION</span></span>
<span data-ttu-id="d3af6-106">Командлет **Get-AzureRemoteAppOperationResult** получает результат длительной операции с приложением RemoteApp Azure.</span><span class="sxs-lookup"><span data-stu-id="d3af6-106">The **Get-AzureRemoteAppOperationResult** cmdlet retrieves the result of a long-running Azure RemoteApp operation.</span></span>
<span data-ttu-id="d3af6-107">Приложение Azure RemoteApp использует длительные операции для множества действий, требующих обработки службой, и не может возвращаться немедленно.</span><span class="sxs-lookup"><span data-stu-id="d3af6-107">Azure RemoteApp uses long-running operations for many actions that require processing by the service and cannot return immediately.</span></span>
<span data-ttu-id="d3af6-108">Ниже приведены примеры командлетов, возвращающих идентификаторы отслеживания: **Update-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** и другие.</span><span class="sxs-lookup"><span data-stu-id="d3af6-108">Examples of cmdlets that return tracking IDs include **Update-AzureRemoteAppCollection** , **Set-AzureRemoteAppWorkspace** , **Disconnect-AzureRemoteAppSession** , and others.</span></span>

## <span data-ttu-id="d3af6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d3af6-109">EXAMPLES</span></span>

### <span data-ttu-id="d3af6-110">Пример 1: использование идентификатора отслеживания для получения результата операции</span><span class="sxs-lookup"><span data-stu-id="d3af6-110">Example 1: Use a tracking ID to get an operation result</span></span>
```
PS C:\> $result = New-AzureRemoteAppCollection -CollectionName Contoso -ImageName "Windows Server 2012 R2" -Plan Standard -Location "West US" -Description CloudOnly
PS C:\> Get-AzureRemoteAppOperationResult -TrackingId $result.Tracking
```

<span data-ttu-id="d3af6-111">Эта команда сохраняет ИД отслеживания, возвращенный операцией Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="d3af6-111">This command saves the tracking ID returned from an Azure RemoteApp operation.</span></span>
<span data-ttu-id="d3af6-112">ИДЕНТИФИКАТОР отслеживания передается в **Get-AzureRemoteAppOperationResult** в следующей команде.</span><span class="sxs-lookup"><span data-stu-id="d3af6-112">The tracking ID is passed to **Get-AzureRemoteAppOperationResult** in the command that follows.</span></span>

## <span data-ttu-id="d3af6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d3af6-113">PARAMETERS</span></span>

### <span data-ttu-id="d3af6-114">-Profile</span><span class="sxs-lookup"><span data-stu-id="d3af6-114">-Profile</span></span>
<span data-ttu-id="d3af6-115">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d3af6-115">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d3af6-116">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d3af6-116">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d3af6-117">-TrackingId</span><span class="sxs-lookup"><span data-stu-id="d3af6-117">-TrackingId</span></span>
<span data-ttu-id="d3af6-118">Указывает код отслеживания для операции.</span><span class="sxs-lookup"><span data-stu-id="d3af6-118">Specifies the tracking ID of an operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3af6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3af6-119">CommonParameters</span></span>
<span data-ttu-id="d3af6-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d3af6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3af6-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3af6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3af6-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d3af6-122">INPUTS</span></span>

## <span data-ttu-id="d3af6-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d3af6-123">OUTPUTS</span></span>

## <span data-ttu-id="d3af6-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="d3af6-124">NOTES</span></span>

## <span data-ttu-id="d3af6-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d3af6-125">RELATED LINKS</span></span>

[<span data-ttu-id="d3af6-126">Разъединить — AzureRemoteAppSession</span><span class="sxs-lookup"><span data-stu-id="d3af6-126">Disconnect-AzureRemoteAppSession</span></span>](./Disconnect-AzureRemoteAppSession.md)

[<span data-ttu-id="d3af6-127">Set-AzureRemoteAppWorkspace</span><span class="sxs-lookup"><span data-stu-id="d3af6-127">Set-AzureRemoteAppWorkspace</span></span>](./Set-AzureRemoteAppWorkspace.md)

[<span data-ttu-id="d3af6-128">Update-AzureRemoteAppCollection</span><span class="sxs-lookup"><span data-stu-id="d3af6-128">Update-AzureRemoteAppCollection</span></span>](./Update-AzureRemoteAppCollection.md)



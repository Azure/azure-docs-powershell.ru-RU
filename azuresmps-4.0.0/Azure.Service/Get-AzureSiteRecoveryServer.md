---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4081d6d072aadd6a4ae7d09ff57748a8f2cb697
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075580"
---
# <span data-ttu-id="8ec85-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="8ec85-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="8ec85-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8ec85-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec85-103">Возвращает серверы восстановления сайта, которые зарегистрировали хранилище сайтов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="8ec85-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="8ec85-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8ec85-104">SYNTAX</span></span>

### <span data-ttu-id="8ec85-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ec85-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8ec85-106">ById</span><span class="sxs-lookup"><span data-stu-id="8ec85-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8ec85-107">ByName</span><span class="sxs-lookup"><span data-stu-id="8ec85-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8ec85-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ec85-108">DESCRIPTION</span></span>
<span data-ttu-id="8ec85-109">Командлет **Get-AzureSiteRecoveryServer** получает сведения о серверах Azure Site Recovery, зарегистрированных в текущем хранилище сайта для восстановления.</span><span class="sxs-lookup"><span data-stu-id="8ec85-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="8ec85-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8ec85-110">EXAMPLES</span></span>

### <span data-ttu-id="8ec85-111">Пример 1: получение сведений о сервере восстановления сайта</span><span class="sxs-lookup"><span data-stu-id="8ec85-111">Example 1: Get information about a Site Recovery server</span></span>
```
PS C:\> Get-AzureSiteRecoveryServer
ID              : cd7dec80-1144-4531-9ab3-888b8ab39bee
Name            : server1.contoso.com
LastHeartbeat   : 9/23/2014 3:51:22 PM
ProviderVersion : 3.5.520.0
ServerVersion   : 3.2.7634.0

ID              : f5e713fe-5b6d-4641-9690-6fe74c976b8e
Name            : Server2.contoso.com
LastHeartbeat   : 8/13/2014 2:28:58 PM
ProviderVersion : 3.5
ServerVersion   : 3.2.7510.0
```

<span data-ttu-id="8ec85-112">Эта команда получает сведения о сервере Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8ec85-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="8ec85-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8ec85-113">PARAMETERS</span></span>

### <span data-ttu-id="8ec85-114">-ID</span><span class="sxs-lookup"><span data-stu-id="8ec85-114">-Id</span></span>
<span data-ttu-id="8ec85-115">Указывает идентификатор сервера.</span><span class="sxs-lookup"><span data-stu-id="8ec85-115">Specifies the ID of a server.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec85-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8ec85-116">-Name</span></span>
<span data-ttu-id="8ec85-117">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="8ec85-117">Specifies the name of a server.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ec85-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="8ec85-118">-Profile</span></span>
<span data-ttu-id="8ec85-119">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8ec85-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8ec85-120">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ec85-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8ec85-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec85-121">CommonParameters</span></span>
<span data-ttu-id="8ec85-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8ec85-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec85-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec85-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec85-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8ec85-124">INPUTS</span></span>

## <span data-ttu-id="8ec85-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ec85-125">OUTPUTS</span></span>

## <span data-ttu-id="8ec85-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="8ec85-126">NOTES</span></span>

## <span data-ttu-id="8ec85-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ec85-127">RELATED LINKS</span></span>

[<span data-ttu-id="8ec85-128">Командлеты служб Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="8ec85-128">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)



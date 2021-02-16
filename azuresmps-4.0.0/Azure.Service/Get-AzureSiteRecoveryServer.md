---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 3EC274C9-9BF6-4B39-BC70-C7F9D780805D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79b61501a56913fedb2a003d7aea1a041bfab4d5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412288"
---
# <span data-ttu-id="c375a-101">Get-AzureSiteRecoveryServer</span><span class="sxs-lookup"><span data-stu-id="c375a-101">Get-AzureSiteRecoveryServer</span></span>

## <span data-ttu-id="c375a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c375a-102">SYNOPSIS</span></span>
<span data-ttu-id="c375a-103">Регистрирует серверы восстановления сайта в хранилище восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="c375a-103">Gets Site Recovery servers registered a Site Recovery vault.</span></span>

## <span data-ttu-id="c375a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c375a-104">SYNTAX</span></span>

### <span data-ttu-id="c375a-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c375a-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryServer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c375a-106">ById</span><span class="sxs-lookup"><span data-stu-id="c375a-106">ById</span></span>
```
Get-AzureSiteRecoveryServer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="c375a-107">ByName</span><span class="sxs-lookup"><span data-stu-id="c375a-107">ByName</span></span>
```
Get-AzureSiteRecoveryServer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c375a-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c375a-108">DESCRIPTION</span></span>
<span data-ttu-id="c375a-109">С **его учетом** можно получить сведения о серверах восстановления сайтов Azure, зарегистрированных в текущем хранилище восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="c375a-109">The **Get-AzureSiteRecoveryServer** cmdlet gets information about Azure Site Recovery servers registered to the current Site Recovery vault.</span></span>

## <span data-ttu-id="c375a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c375a-110">EXAMPLES</span></span>

### <span data-ttu-id="c375a-111">Пример 1. Просмотр сведений о сервере восстановления сайта</span><span class="sxs-lookup"><span data-stu-id="c375a-111">Example 1: Get information about a Site Recovery server</span></span>
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

<span data-ttu-id="c375a-112">Эта команда получает сведения о сервере восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="c375a-112">This command gets information about an Azure Site Recovery server.</span></span>

## <span data-ttu-id="c375a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c375a-113">PARAMETERS</span></span>

### <span data-ttu-id="c375a-114">-Id</span><span class="sxs-lookup"><span data-stu-id="c375a-114">-Id</span></span>
<span data-ttu-id="c375a-115">Определяет ИД сервера.</span><span class="sxs-lookup"><span data-stu-id="c375a-115">Specifies the ID of a server.</span></span>

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

### <span data-ttu-id="c375a-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c375a-116">-Name</span></span>
<span data-ttu-id="c375a-117">Указывает имя сервера.</span><span class="sxs-lookup"><span data-stu-id="c375a-117">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="c375a-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="c375a-118">-Profile</span></span>
<span data-ttu-id="c375a-119">Определяет профиль Azure, для которого читается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c375a-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c375a-120">Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c375a-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c375a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c375a-121">CommonParameters</span></span>
<span data-ttu-id="c375a-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c375a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c375a-123">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c375a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c375a-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c375a-124">INPUTS</span></span>

## <span data-ttu-id="c375a-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c375a-125">OUTPUTS</span></span>

## <span data-ttu-id="c375a-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c375a-126">NOTES</span></span>

## <span data-ttu-id="c375a-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c375a-127">RELATED LINKS</span></span>





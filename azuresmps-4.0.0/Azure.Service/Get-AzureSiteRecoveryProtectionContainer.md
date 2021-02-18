---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: ee948161f101b83a4892441286b760a044e64358
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405828"
---
# <span data-ttu-id="5daaf-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5daaf-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="5daaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5daaf-102">SYNOPSIS</span></span>
<span data-ttu-id="5daaf-103">Получает контейнеры защиты для хранилища восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="5daaf-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="5daaf-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5daaf-104">SYNTAX</span></span>

### <span data-ttu-id="5daaf-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5daaf-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5daaf-106">ById</span><span class="sxs-lookup"><span data-stu-id="5daaf-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5daaf-107">ByName</span><span class="sxs-lookup"><span data-stu-id="5daaf-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5daaf-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5daaf-108">DESCRIPTION</span></span>
<span data-ttu-id="5daaf-109">Чтобы получить контейнеры защиты для текущего хранилища для восстановления сайтов Azure, можно получить с его использованием проектлет **Get-AzureSiteRecoveryProtectionContainer.**</span><span class="sxs-lookup"><span data-stu-id="5daaf-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="5daaf-110">Контейнер защиты — это логический контейнер для защищенных объектов, таких как виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="5daaf-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="5daaf-111">Политики защиты определяют параметры репликации для защищенных элементов и могут быть связаны с контейнером защиты и применены к защищенной сущности.</span><span class="sxs-lookup"><span data-stu-id="5daaf-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="5daaf-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5daaf-112">EXAMPLES</span></span>

### <span data-ttu-id="5daaf-113">Пример 1. Защита контейнеров</span><span class="sxs-lookup"><span data-stu-id="5daaf-113">Example 1: Get protected containers</span></span>
```
PS C:\> Get-AzureSiteRecoveryProtectionContainer
Name                        : PrimaryCloud
ID                          : fd00d920-79e4-4f2d-a282-a779c0cecb7f_ce995917-c962-45d0-b7f3-9f408a4e1429
FabricObjectId              : fd00d920-79e4-4f2d-a282-a779c0cecb7f
FabricType                  : VMM
Type                        : VMM
ServerId                    : fd00d920-79e4-4f2d-a282-a779c0cecb7f
Role                        : Primary
AvailableProtectionProfiles : {ab01dcbe-9da0-4c31-9564-d6904cfadfde, ad388147-83de-4d2f-a09d-fa46c626747e}
```

<span data-ttu-id="5daaf-114">Эта команда получает защищенные контейнеры для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="5daaf-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="5daaf-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5daaf-115">PARAMETERS</span></span>

### <span data-ttu-id="5daaf-116">-Id</span><span class="sxs-lookup"><span data-stu-id="5daaf-116">-Id</span></span>
<span data-ttu-id="5daaf-117">Определяет ID защищенного контейнера, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="5daaf-117">Specifies the ID of a protected container to get.</span></span>

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

### <span data-ttu-id="5daaf-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5daaf-118">-Name</span></span>
<span data-ttu-id="5daaf-119">Указывает имя контейнера защиты, который нужно получить.</span><span class="sxs-lookup"><span data-stu-id="5daaf-119">Specifies the name of a protection container to get.</span></span>

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

### <span data-ttu-id="5daaf-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="5daaf-120">-Profile</span></span>
<span data-ttu-id="5daaf-121">Определяет профиль Azure, для которого читается этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5daaf-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5daaf-122">Если не указать профиль, этот cmdlet будет читать данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5daaf-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5daaf-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5daaf-123">CommonParameters</span></span>
<span data-ttu-id="5daaf-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5daaf-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5daaf-125">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5daaf-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5daaf-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5daaf-126">INPUTS</span></span>

## <span data-ttu-id="5daaf-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5daaf-127">OUTPUTS</span></span>

## <span data-ttu-id="5daaf-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5daaf-128">NOTES</span></span>

## <span data-ttu-id="5daaf-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5daaf-129">RELATED LINKS</span></span>





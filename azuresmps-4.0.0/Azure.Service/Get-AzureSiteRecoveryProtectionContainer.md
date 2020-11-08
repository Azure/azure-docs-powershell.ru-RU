---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 02396628-5E3E-49A6-8377-3F6DC488FEF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75a083c2f892b7b4f07c37ef978d1babb1dd0cb0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/18/2020
ms.locfileid: "94075593"
---
# <span data-ttu-id="2b49c-101">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2b49c-101">Get-AzureSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="2b49c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b49c-102">SYNOPSIS</span></span>
<span data-ttu-id="2b49c-103">Получает контейнеры защиты для хранилища сайта для восстановления.</span><span class="sxs-lookup"><span data-stu-id="2b49c-103">Gets protection containers for a Site Recovery vault.</span></span>

## <span data-ttu-id="2b49c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b49c-104">SYNTAX</span></span>

### <span data-ttu-id="2b49c-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2b49c-105">Default (Default)</span></span>
```
Get-AzureSiteRecoveryProtectionContainer [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b49c-106">ById</span><span class="sxs-lookup"><span data-stu-id="2b49c-106">ById</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2b49c-107">ByName</span><span class="sxs-lookup"><span data-stu-id="2b49c-107">ByName</span></span>
```
Get-AzureSiteRecoveryProtectionContainer -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="2b49c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b49c-108">DESCRIPTION</span></span>
<span data-ttu-id="2b49c-109">Командлет **Get-AzureSiteRecoveryProtectionContainer** получает контейнеры защиты для текущего хранилища Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="2b49c-109">The **Get-AzureSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="2b49c-110">Контейнер защиты — это логический контейнер для защищенных объектов, таких как виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="2b49c-110">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="2b49c-111">Политики защиты определяют параметры репликации для защищенных элементов и могут быть связаны с контейнером защиты и применяются к защищенному объекту.</span><span class="sxs-lookup"><span data-stu-id="2b49c-111">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="2b49c-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b49c-112">EXAMPLES</span></span>

### <span data-ttu-id="2b49c-113">Пример 1: получение защищенных контейнеров</span><span class="sxs-lookup"><span data-stu-id="2b49c-113">Example 1: Get protected containers</span></span>
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

<span data-ttu-id="2b49c-114">Эта команда получает защищенные контейнеры для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="2b49c-114">This command gets the protected containers for the current vault.</span></span>

## <span data-ttu-id="2b49c-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b49c-115">PARAMETERS</span></span>

### <span data-ttu-id="2b49c-116">-ID</span><span class="sxs-lookup"><span data-stu-id="2b49c-116">-Id</span></span>
<span data-ttu-id="2b49c-117">Указывает идентификатор защищенного контейнера, который требуется получить.</span><span class="sxs-lookup"><span data-stu-id="2b49c-117">Specifies the ID of a protected container to get.</span></span>

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

### <span data-ttu-id="2b49c-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2b49c-118">-Name</span></span>
<span data-ttu-id="2b49c-119">Указывает имя контейнера защиты, которое нужно получить.</span><span class="sxs-lookup"><span data-stu-id="2b49c-119">Specifies the name of a protection container to get.</span></span>

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

### <span data-ttu-id="2b49c-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="2b49c-120">-Profile</span></span>
<span data-ttu-id="2b49c-121">Указывает профиль Azure, из которого считывается этот командлет.</span><span class="sxs-lookup"><span data-stu-id="2b49c-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2b49c-122">Если вы не укажете профиль, этот командлет считывает данные из локального профиля по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2b49c-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2b49c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b49c-123">CommonParameters</span></span>
<span data-ttu-id="2b49c-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b49c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b49c-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b49c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b49c-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b49c-126">INPUTS</span></span>

## <span data-ttu-id="2b49c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b49c-127">OUTPUTS</span></span>

## <span data-ttu-id="2b49c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b49c-128">NOTES</span></span>

## <span data-ttu-id="2b49c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b49c-129">RELATED LINKS</span></span>

[<span data-ttu-id="2b49c-130">Командлеты служб Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="2b49c-130">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)



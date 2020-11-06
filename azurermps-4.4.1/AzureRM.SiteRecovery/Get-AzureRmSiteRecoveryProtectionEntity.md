---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 706b1ba37d7ac31215e5ecb07f3941e7e89ede5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569188"
---
# <span data-ttu-id="b2274-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b2274-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="b2274-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2274-102">SYNOPSIS</span></span>
<span data-ttu-id="b2274-103">Получает список защищаемых или защищенных сущностей в текущем хранилище для восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="b2274-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2274-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2274-104">SYNTAX</span></span>

### <span data-ttu-id="b2274-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b2274-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2274-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b2274-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2274-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="b2274-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2274-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2274-108">DESCRIPTION</span></span>
<span data-ttu-id="b2274-109">Командлет **Get-AzureRmSiteRecoveryProtectionEntity** получает список защищаемых или защищенных объектов, например виртуальных машин, в текущем хранилище Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="b2274-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="b2274-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2274-110">EXAMPLES</span></span>

## <span data-ttu-id="b2274-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2274-111">PARAMETERS</span></span>

### <span data-ttu-id="b2274-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b2274-112">-FriendlyName</span></span>
<span data-ttu-id="b2274-113">Указывает понятное имя для объекта защиты.</span><span class="sxs-lookup"><span data-stu-id="b2274-113">Specifies the friendly name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2274-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b2274-114">-Name</span></span>
<span data-ttu-id="b2274-115">Указывает имя объекта защиты.</span><span class="sxs-lookup"><span data-stu-id="b2274-115">Specifies the name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2274-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b2274-116">-ProtectionContainer</span></span>
<span data-ttu-id="b2274-117">Указывает объект контейнера защиты.</span><span class="sxs-lookup"><span data-stu-id="b2274-117">Specifies the protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2274-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2274-118">-DefaultProfile</span></span>
<span data-ttu-id="b2274-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2274-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2274-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2274-120">CommonParameters</span></span>
<span data-ttu-id="b2274-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2274-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2274-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2274-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2274-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2274-123">INPUTS</span></span>

### <span data-ttu-id="b2274-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="b2274-124">ASRProtectionContainer</span></span>
<span data-ttu-id="b2274-125">Параметр "ProtectionContainer" принимает значение типа "ASRProtectionContainer" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b2274-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="b2274-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2274-126">OUTPUTS</span></span>

### <span data-ttu-id="b2274-127">System. Collections. Generic. IEnumerable 1 [Microsoft. Azure. Commands. SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="b2274-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="b2274-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2274-128">NOTES</span></span>

## <span data-ttu-id="b2274-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2274-129">RELATED LINKS</span></span>

[<span data-ttu-id="b2274-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="b2274-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)

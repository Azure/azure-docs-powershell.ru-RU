---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7B8C8239-16A3-4C47-9D6F-DE31885532F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADServicePrincipal.md
ms.openlocfilehash: 853404bce6d45f2824c574b249c434ccebc281ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567934"
---
# <span data-ttu-id="e0ba7-101">Set-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e0ba7-101">Set-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="e0ba7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ba7-103">Обновление существующего субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0ba7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0ba7-104">SYNTAX</span></span>

### <span data-ttu-id="e0ba7-105">SpObjectIdWithDisplayNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0ba7-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0ba7-106">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0ba7-106">SPNWithDisplayNameParameterSet</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName <String> -DisplayName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0ba7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0ba7-107">DESCRIPTION</span></span>
<span data-ttu-id="e0ba7-108">Обновление существующего субъекта-службы Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-108">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="e0ba7-109">Чтобы обновить учетные данные, связанные с этим субъектом-службой, используйте командлет New-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-109">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="e0ba7-110">Чтобы обновить свойства, связанные с основным приложением, используйте командлет Set-AzureRmADApplication.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-110">To update the properties associated with the underlying application, please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="e0ba7-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0ba7-111">EXAMPLES</span></span>

### <span data-ttu-id="e0ba7-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e0ba7-112">Example 1</span></span>
```
Set-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName "UpdatedNameForSp"
```

<span data-ttu-id="e0ba7-113">Обновляет отображаемое имя субъекта-службы с указанным идентификатором объекта.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-113">Updates the display name for the service principal with specified object id.</span></span>

### <span data-ttu-id="e0ba7-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e0ba7-114">Example 2</span></span>
```
Set-AzureRmADServicePrincipal -ServicePrincipalName "http://MyApp1" -DisplayName "UpdatedNameforSp"
```

<span data-ttu-id="e0ba7-115">Обновление отображаемого имени субъекта-службы с указанным именем субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-115">Updates the display name for the service principal with specified service principal name.</span></span>

## <span data-ttu-id="e0ba7-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0ba7-116">PARAMETERS</span></span>

### <span data-ttu-id="e0ba7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ba7-117">-DefaultProfile</span></span>
<span data-ttu-id="e0ba7-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e0ba7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ba7-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e0ba7-119">-DisplayName</span></span>
<span data-ttu-id="e0ba7-120">Новое отображаемое имя субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-120">New display name for the service principal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ba7-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e0ba7-121">-ObjectId</span></span>
<span data-ttu-id="e0ba7-122">Идентификатор объекта субъекта-службы, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-122">The object id of the service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ba7-123">-Намерено</span><span class="sxs-lookup"><span data-stu-id="e0ba7-123">-ServicePrincipalName</span></span>
<span data-ttu-id="e0ba7-124">SPN субъекта-службы для обновления.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-124">The SPN of service principal to update.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0ba7-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0ba7-125">-Confirm</span></span>
<span data-ttu-id="e0ba7-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ba7-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0ba7-127">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ba7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ba7-128">CommonParameters</span></span>
<span data-ttu-id="e0ba7-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ba7-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0ba7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ba7-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0ba7-131">INPUTS</span></span>

### <span data-ttu-id="e0ba7-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="e0ba7-132">None</span></span>
<span data-ttu-id="e0ba7-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="e0ba7-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e0ba7-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0ba7-134">OUTPUTS</span></span>

## <span data-ttu-id="e0ba7-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0ba7-135">NOTES</span></span>

## <span data-ttu-id="e0ba7-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0ba7-136">RELATED LINKS</span></span>

[<span data-ttu-id="e0ba7-137">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e0ba7-137">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e0ba7-138">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e0ba7-138">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e0ba7-139">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e0ba7-139">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="e0ba7-140">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e0ba7-140">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="e0ba7-141">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e0ba7-141">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="e0ba7-142">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e0ba7-142">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)


---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: 0cfcb2713eaac255f625b09c0ba81883242f48aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558844"
---
# <span data-ttu-id="42514-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="42514-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="42514-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42514-102">SYNOPSIS</span></span>
<span data-ttu-id="42514-103">Удаление учетных данных из приложения.</span><span class="sxs-lookup"><span data-stu-id="42514-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42514-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42514-104">SYNTAX</span></span>

### <span data-ttu-id="42514-105">ApplicationObjectIdWithKeyIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42514-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42514-106">ApplicationObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="42514-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42514-107">ApplicationIdWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42514-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42514-108">ApplicationIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="42514-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42514-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42514-109">DESCRIPTION</span></span>
<span data-ttu-id="42514-110">Командлет Remove-AzureRmADAppCredential можно использовать для удаления ключа учетных данных из приложения в случае раскрытия или в рамках истечения срока действия смены ключа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="42514-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="42514-111">Приложение определяется путем указания идентификатора объекта или AppId.</span><span class="sxs-lookup"><span data-stu-id="42514-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="42514-112">Учетные данные, которые нужно удалить, определяются с помощью идентификатора ключа, если необходимо удалить индивидуальные учетные данные или с помощью переключателя "все" для удаления всех учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="42514-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="42514-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42514-113">EXAMPLES</span></span>

### <span data-ttu-id="42514-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42514-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="42514-115">Эта команда удаляет ключ учетных данных из приложения.</span><span class="sxs-lookup"><span data-stu-id="42514-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="42514-116">В этом примере ключ с идентификатором "9044423a-60a3-45AC-9ab1-09534157ebb" будет удален из приложения.</span><span class="sxs-lookup"><span data-stu-id="42514-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="42514-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="42514-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="42514-118">Эта команда удаляет ключ учетных данных из приложения.</span><span class="sxs-lookup"><span data-stu-id="42514-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="42514-119">В этом примере все учетные данные будут удалены из приложения, связанного с applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="42514-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="42514-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42514-120">PARAMETERS</span></span>

### <span data-ttu-id="42514-121">-ALL</span><span class="sxs-lookup"><span data-stu-id="42514-121">-All</span></span>
<span data-ttu-id="42514-122">Переключиться на удаление всех учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="42514-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42514-123">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="42514-123">-ApplicationId</span></span>
<span data-ttu-id="42514-124">Идентификатор приложения, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="42514-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42514-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42514-125">-DefaultProfile</span></span>
<span data-ttu-id="42514-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="42514-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42514-127">-Force</span><span class="sxs-lookup"><span data-stu-id="42514-127">-Force</span></span>
<span data-ttu-id="42514-128">Переключиться в режим удаления учетных данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="42514-128">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42514-129">-KeyId</span><span class="sxs-lookup"><span data-stu-id="42514-129">-KeyId</span></span>
<span data-ttu-id="42514-130">Указывает ключ учетных данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="42514-130">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="42514-131">Коды клавиш для приложения можно получить с помощью командлета Get-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="42514-131">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42514-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="42514-132">-ObjectId</span></span>
<span data-ttu-id="42514-133">Идентификатор объекта приложения, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="42514-133">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42514-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42514-134">-Confirm</span></span>
<span data-ttu-id="42514-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="42514-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42514-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42514-136">-WhatIf</span></span>
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

### <span data-ttu-id="42514-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42514-137">CommonParameters</span></span>
<span data-ttu-id="42514-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42514-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42514-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42514-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42514-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42514-140">INPUTS</span></span>

### <span data-ttu-id="42514-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="42514-141">None</span></span>
<span data-ttu-id="42514-142">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="42514-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42514-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42514-143">OUTPUTS</span></span>

## <span data-ttu-id="42514-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="42514-144">NOTES</span></span>

## <span data-ttu-id="42514-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42514-145">RELATED LINKS</span></span>

[<span data-ttu-id="42514-146">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="42514-146">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="42514-147">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="42514-147">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="42514-148">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="42514-148">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

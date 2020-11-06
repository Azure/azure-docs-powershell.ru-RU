---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: bfda87b4a0810dc440da63949d17f52cf611fa19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567946"
---
# <span data-ttu-id="c4041-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c4041-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="c4041-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4041-102">SYNOPSIS</span></span>
<span data-ttu-id="c4041-103">Удаление учетных данных из субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="c4041-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4041-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4041-104">SYNTAX</span></span>

### <span data-ttu-id="c4041-105">ObjectIdWithKeyIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4041-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4041-106">ObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4041-106">ObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4041-107">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4041-107">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4041-108">SPNWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4041-108">SPNWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4041-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4041-109">DESCRIPTION</span></span>
<span data-ttu-id="c4041-110">Командлет Remove-AzureRmADSpCredential можно использовать для удаления ключа учетных данных из субъекта-службы в случае раскрытия или в рамках срока действия ключа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c4041-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="c4041-111">Субъект-служба определяется путем указания либо идентификатора объекта, либо имени субъекта-службы (SPN).</span><span class="sxs-lookup"><span data-stu-id="c4041-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>

<span data-ttu-id="c4041-112">Учетные данные, которые нужно удалить, определяются с помощью идентификатора ключа, если необходимо удалить индивидуальные учетные данные или с помощью переключателя "все" для удаления всех учетных данных, связанных с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="c4041-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="c4041-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4041-113">EXAMPLES</span></span>

### <span data-ttu-id="c4041-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4041-114">Example 1</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="c4041-115">Эта команда удаляет ключ учетных данных из субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="c4041-115">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="c4041-116">В этом примере ключ с идентификатором "9044423a-60a3-45AC-9ab1-09534157ebb" будет удален из субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="c4041-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the service principal.</span></span>

### <span data-ttu-id="c4041-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c4041-117">Example 2</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

<span data-ttu-id="c4041-118">Эта команда удаляет ключ учетных данных из субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="c4041-118">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="c4041-119">В этом примере все учетные данные будут удалены из субъекта-службы, связанного с именем субъекта-службы " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="c4041-119">In this example, all credentials will be removed from the service principal associated with the service principal name "http://test123".</span></span>

## <span data-ttu-id="c4041-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4041-120">PARAMETERS</span></span>

### <span data-ttu-id="c4041-121">-ALL</span><span class="sxs-lookup"><span data-stu-id="c4041-121">-All</span></span>
<span data-ttu-id="c4041-122">Выберите параметр, чтобы удалить все учетные данные, связанные с субъектом-службу.</span><span class="sxs-lookup"><span data-stu-id="c4041-122">Switch to remove all the credentials associated with the service principal.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4041-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4041-123">-DefaultProfile</span></span>
<span data-ttu-id="c4041-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c4041-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4041-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c4041-125">-Force</span></span>
<span data-ttu-id="c4041-126">Переключиться в режим удаления учетных данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c4041-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="c4041-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c4041-127">-KeyId</span></span>
<span data-ttu-id="c4041-128">Указывает ключ учетных данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c4041-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="c4041-129">Идентификаторы ключей для субъекта-службы можно получить с помощью командлета Get-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="c4041-129">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4041-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c4041-130">-ObjectId</span></span>
<span data-ttu-id="c4041-131">Идентификатор объекта субъекта-службы, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c4041-131">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4041-132">-Намерено</span><span class="sxs-lookup"><span data-stu-id="c4041-132">-ServicePrincipalName</span></span>
<span data-ttu-id="c4041-133">Имя (SPN) субъекта-службы, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="c4041-133">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4041-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4041-134">-Confirm</span></span>
<span data-ttu-id="c4041-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c4041-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4041-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4041-136">-WhatIf</span></span>
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

### <span data-ttu-id="c4041-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4041-137">CommonParameters</span></span>
<span data-ttu-id="c4041-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4041-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4041-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4041-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4041-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4041-140">INPUTS</span></span>

### <span data-ttu-id="c4041-141">Ничего</span><span class="sxs-lookup"><span data-stu-id="c4041-141">None</span></span>
<span data-ttu-id="c4041-142">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c4041-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c4041-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4041-143">OUTPUTS</span></span>

## <span data-ttu-id="c4041-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4041-144">NOTES</span></span>

## <span data-ttu-id="c4041-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4041-145">RELATED LINKS</span></span>

[<span data-ttu-id="c4041-146">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c4041-146">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="c4041-147">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c4041-147">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="c4041-148">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c4041-148">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)


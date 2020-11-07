---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 04B1E3A6-6D52-46A3-8241-2CCDB5E71642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADSpCredential.md
ms.openlocfilehash: b1f4b8d53a1031cef76d51a87bbf9afa5b75758f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734247"
---
# <span data-ttu-id="0d5b0-101">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0d5b0-101">Remove-AzureRmADSpCredential</span></span>

## <span data-ttu-id="0d5b0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5b0-103">Удаление учетных данных из субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-103">Removes a credential from a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d5b0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d5b0-104">SYNTAX</span></span>

### <span data-ttu-id="0d5b0-105">ObjectIdWithKeyIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d5b0-105">ObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d5b0-106">ObjectIdWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d5b0-106">ObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d5b0-107">SPNWithKeyIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d5b0-107">SPNWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d5b0-108">SPNWithAllParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d5b0-108">SPNWithAllParameterSet</span></span>
```
Remove-AzureRmADSpCredential -ServicePrincipalName <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d5b0-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d5b0-109">DESCRIPTION</span></span>
<span data-ttu-id="0d5b0-110">Командлет Remove-AzureRmADSpCredential можно использовать для удаления ключа учетных данных из субъекта-службы в случае раскрытия или в рамках срока действия ключа учетных данных.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-110">The Remove-AzureRmADSpCredential cmdlet can be used to remove a credential key from a service principal in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="0d5b0-111">Субъект-служба определяется путем указания либо идентификатора объекта, либо имени субъекта-службы (SPN).</span><span class="sxs-lookup"><span data-stu-id="0d5b0-111">The service principal is identified by supplying either the object ID or service principal name (SPN).</span></span>

<span data-ttu-id="0d5b0-112">Учетные данные, которые нужно удалить, определяются с помощью идентификатора ключа, если необходимо удалить индивидуальные учетные данные или с помощью переключателя "все" для удаления всех учетных данных, связанных с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the service principal.</span></span>

## <span data-ttu-id="0d5b0-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d5b0-113">EXAMPLES</span></span>

### <span data-ttu-id="0d5b0-114">--------------------------Пример 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0d5b0-114">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="0d5b0-115">Эта команда удаляет ключ учетных данных из субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-115">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="0d5b0-116">В этом примере ключ с идентификатором "9044423a-60a3-45AC-9ab1-09534157ebb" будет удален из субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the service principal.</span></span>

### <span data-ttu-id="0d5b0-117">--------------------------Пример 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0d5b0-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADSpCredential -ServicePrincipalName http://test123 -All
```

<span data-ttu-id="0d5b0-118">Эта команда удаляет ключ учетных данных из субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-118">This command removes a credential key from a service principal.</span></span>
<span data-ttu-id="0d5b0-119">В этом примере все учетные данные будут удалены из субъекта-службы, связанного с именем субъекта-службы " http://test123 ".</span><span class="sxs-lookup"><span data-stu-id="0d5b0-119">In this example, all credentials will be removed from the service principal associated with the service principal name "http://test123".</span></span>

## <span data-ttu-id="0d5b0-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d5b0-120">PARAMETERS</span></span>

### <span data-ttu-id="0d5b0-121">-ALL</span><span class="sxs-lookup"><span data-stu-id="0d5b0-121">-All</span></span>
<span data-ttu-id="0d5b0-122">Выберите параметр, чтобы удалить все учетные данные, связанные с субъектом-службу.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-122">Switch to remove all the credentials associated with the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ObjectIdWithAllParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5b0-123">-Force</span><span class="sxs-lookup"><span data-stu-id="0d5b0-123">-Force</span></span>
<span data-ttu-id="0d5b0-124">Переключиться в режим удаления учетных данных без подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-124">Switch to delete credential without a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d5b0-125">-KeyId</span><span class="sxs-lookup"><span data-stu-id="0d5b0-125">-KeyId</span></span>
<span data-ttu-id="0d5b0-126">Указывает ключ учетных данных, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-126">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="0d5b0-127">Идентификаторы ключей для субъекта-службы можно получить с помощью командлета Get-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-127">The key Ids for a service principal can be obtained using the Get-AzureRmADSpCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdWithKeyIdParameterSet, SPNWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5b0-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0d5b0-128">-ObjectId</span></span>
<span data-ttu-id="0d5b0-129">Идентификатор объекта субъекта-службы, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-129">The object id of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdWithKeyIdParameterSet, ObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5b0-130">-Намерено</span><span class="sxs-lookup"><span data-stu-id="0d5b0-130">-ServicePrincipalName</span></span>
<span data-ttu-id="0d5b0-131">Имя (SPN) субъекта-службы, из которого нужно удалить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-131">The name (SPN) of the service principal to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithKeyIdParameterSet, SPNWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5b0-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d5b0-132">-Confirm</span></span>
<span data-ttu-id="0d5b0-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d5b0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d5b0-134">-WhatIf</span></span>
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d5b0-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5b0-135">-DefaultProfile</span></span>
<span data-ttu-id="0d5b0-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d5b0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5b0-137">CommonParameters</span></span>
<span data-ttu-id="0d5b0-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d5b0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5b0-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d5b0-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5b0-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d5b0-140">INPUTS</span></span>

## <span data-ttu-id="0d5b0-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d5b0-141">OUTPUTS</span></span>

## <span data-ttu-id="0d5b0-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d5b0-142">NOTES</span></span>

## <span data-ttu-id="0d5b0-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d5b0-143">RELATED LINKS</span></span>

[<span data-ttu-id="0d5b0-144">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0d5b0-144">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="0d5b0-145">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0d5b0-145">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="0d5b0-146">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0d5b0-146">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)


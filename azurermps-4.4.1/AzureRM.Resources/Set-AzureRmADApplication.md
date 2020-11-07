---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: 6fbbed83f9565a81b305df5cf8b66fd8210c6aec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734779"
---
# <span data-ttu-id="50dc6-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="50dc6-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="50dc6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="50dc6-102">SYNOPSIS</span></span>
<span data-ttu-id="50dc6-103">Обновляет существующее приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50dc6-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50dc6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="50dc6-104">SYNTAX</span></span>

### <span data-ttu-id="50dc6-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="50dc6-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50dc6-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="50dc6-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50dc6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="50dc6-107">DESCRIPTION</span></span>
<span data-ttu-id="50dc6-108">Обновляет существующее приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="50dc6-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="50dc6-109">Чтобы обновить учетные данные, связанные с этим приложением, используйте командлет New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="50dc6-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="50dc6-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="50dc6-110">EXAMPLES</span></span>

### <span data-ttu-id="50dc6-111">--------------------------Пример 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="50dc6-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="50dc6-112">Обновляет свойства существующего приложения Azure Active Directory с objectId "fb7b3405-CA44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="50dc6-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="50dc6-113">--------------------------Пример 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="50dc6-113">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="50dc6-114">Обновление отображаемого имени существующего приложения Azure Active Directory с objectId "fb7b3405-CA44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="50dc6-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="50dc6-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="50dc6-115">PARAMETERS</span></span>

### <span data-ttu-id="50dc6-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="50dc6-116">-ApplicationId</span></span>
<span data-ttu-id="50dc6-117">Идентификатор обновляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="50dc6-117">The id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50dc6-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="50dc6-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="50dc6-119">Значение, указывающее, будет ли приложение обновляться как один клиент или несколько клиентов.</span><span class="sxs-lookup"><span data-stu-id="50dc6-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50dc6-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="50dc6-120">-DisplayName</span></span>
<span data-ttu-id="50dc6-121">Новое отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="50dc6-121">New Display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50dc6-122">-Главная страница</span><span class="sxs-lookup"><span data-stu-id="50dc6-122">-HomePage</span></span>
<span data-ttu-id="50dc6-123">Новый URL-адрес домашней страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="50dc6-123">New URL of the application homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50dc6-124">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="50dc6-124">-IdentifierUris</span></span>
<span data-ttu-id="50dc6-125">Новые универсальные коды ресурсов (URI), обозначающие приложение.</span><span class="sxs-lookup"><span data-stu-id="50dc6-125">New URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50dc6-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="50dc6-126">-ObjectId</span></span>
<span data-ttu-id="50dc6-127">Идентификатор объекта обновляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="50dc6-127">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50dc6-128">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="50dc6-128">-ReplyUrls</span></span>
<span data-ttu-id="50dc6-129">Новые URL-адреса для ответа для приложения.</span><span class="sxs-lookup"><span data-stu-id="50dc6-129">New reply urls for the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50dc6-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="50dc6-130">-Confirm</span></span>
<span data-ttu-id="50dc6-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="50dc6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50dc6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50dc6-132">-WhatIf</span></span>
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

### <span data-ttu-id="50dc6-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50dc6-133">-DefaultProfile</span></span>
<span data-ttu-id="50dc6-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="50dc6-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50dc6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50dc6-135">CommonParameters</span></span>
<span data-ttu-id="50dc6-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="50dc6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50dc6-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50dc6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50dc6-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="50dc6-138">INPUTS</span></span>

## <span data-ttu-id="50dc6-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="50dc6-139">OUTPUTS</span></span>

### <span data-ttu-id="50dc6-140">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="50dc6-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="50dc6-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="50dc6-141">NOTES</span></span>

## <span data-ttu-id="50dc6-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="50dc6-142">RELATED LINKS</span></span>

[<span data-ttu-id="50dc6-143">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="50dc6-143">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="50dc6-144">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="50dc6-144">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="50dc6-145">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="50dc6-145">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="50dc6-146">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="50dc6-146">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="50dc6-147">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="50dc6-147">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="50dc6-148">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="50dc6-148">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)


---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: a8c1aa2d0f22a9c6dc6260384e51140cb930106a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567938"
---
# <span data-ttu-id="f509e-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f509e-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="f509e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f509e-102">SYNOPSIS</span></span>
<span data-ttu-id="f509e-103">Обновляет существующее приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f509e-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f509e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f509e-104">SYNTAX</span></span>

### <span data-ttu-id="f509e-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f509e-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f509e-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f509e-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f509e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f509e-107">DESCRIPTION</span></span>
<span data-ttu-id="f509e-108">Обновляет существующее приложение Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f509e-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="f509e-109">Чтобы обновить учетные данные, связанные с этим приложением, используйте командлет New-AzureRmADAppCredential.</span><span class="sxs-lookup"><span data-stu-id="f509e-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="f509e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f509e-110">EXAMPLES</span></span>

### <span data-ttu-id="f509e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f509e-111">Example 1</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="f509e-112">Обновляет свойства существующего приложения Azure Active Directory с objectId "fb7b3405-CA44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="f509e-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="f509e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f509e-113">Example 2</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="f509e-114">Обновление отображаемого имени существующего приложения Azure Active Directory с objectId "fb7b3405-CA44-4b5b-8584-12392f5d96d7".</span><span class="sxs-lookup"><span data-stu-id="f509e-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="f509e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f509e-115">PARAMETERS</span></span>

### <span data-ttu-id="f509e-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f509e-116">-ApplicationId</span></span>
<span data-ttu-id="f509e-117">Идентификатор обновляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="f509e-117">The id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f509e-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="f509e-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="f509e-119">Значение, указывающее, будет ли приложение обновляться как один клиент или несколько клиентов.</span><span class="sxs-lookup"><span data-stu-id="f509e-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f509e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f509e-120">-DefaultProfile</span></span>
<span data-ttu-id="f509e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f509e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f509e-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f509e-122">-DisplayName</span></span>
<span data-ttu-id="f509e-123">Новое отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="f509e-123">New Display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f509e-124">-Главная страница</span><span class="sxs-lookup"><span data-stu-id="f509e-124">-HomePage</span></span>
<span data-ttu-id="f509e-125">Новый URL-адрес домашней страницы приложения.</span><span class="sxs-lookup"><span data-stu-id="f509e-125">New URL of the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f509e-126">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="f509e-126">-IdentifierUris</span></span>
<span data-ttu-id="f509e-127">Новые универсальные коды ресурсов (URI), обозначающие приложение.</span><span class="sxs-lookup"><span data-stu-id="f509e-127">New URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f509e-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f509e-128">-ObjectId</span></span>
<span data-ttu-id="f509e-129">Идентификатор объекта обновляемого приложения.</span><span class="sxs-lookup"><span data-stu-id="f509e-129">The object id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f509e-130">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="f509e-130">-ReplyUrls</span></span>
<span data-ttu-id="f509e-131">Новые URL-адреса для ответа для приложения.</span><span class="sxs-lookup"><span data-stu-id="f509e-131">New reply urls for the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f509e-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f509e-132">-Confirm</span></span>
<span data-ttu-id="f509e-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f509e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f509e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f509e-134">-WhatIf</span></span>
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

### <span data-ttu-id="f509e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f509e-135">CommonParameters</span></span>
<span data-ttu-id="f509e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f509e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f509e-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f509e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f509e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f509e-138">INPUTS</span></span>

### <span data-ttu-id="f509e-139">Ничего</span><span class="sxs-lookup"><span data-stu-id="f509e-139">None</span></span>
<span data-ttu-id="f509e-140">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f509e-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f509e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f509e-141">OUTPUTS</span></span>

### <span data-ttu-id="f509e-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="f509e-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="f509e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="f509e-143">NOTES</span></span>

## <span data-ttu-id="f509e-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f509e-144">RELATED LINKS</span></span>

[<span data-ttu-id="f509e-145">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f509e-145">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="f509e-146">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f509e-146">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="f509e-147">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="f509e-147">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="f509e-148">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f509e-148">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="f509e-149">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f509e-149">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="f509e-150">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f509e-150">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)


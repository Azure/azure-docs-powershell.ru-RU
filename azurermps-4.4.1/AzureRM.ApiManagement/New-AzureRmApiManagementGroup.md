---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: 8fc237b130e5044e52f47d306d04c42d12fbad81
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565730"
---
# <span data-ttu-id="ae84c-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ae84c-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="ae84c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ae84c-102">SYNOPSIS</span></span>
<span data-ttu-id="ae84c-103">Создание группы управления API.</span><span class="sxs-lookup"><span data-stu-id="ae84c-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae84c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ae84c-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae84c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae84c-105">DESCRIPTION</span></span>
<span data-ttu-id="ae84c-106">Командлет **New-AzureRmApiManagementGroup** создает группу управления API.</span><span class="sxs-lookup"><span data-stu-id="ae84c-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="ae84c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ae84c-107">EXAMPLES</span></span>

### <span data-ttu-id="ae84c-108">Пример 1: создание группы управления</span><span class="sxs-lookup"><span data-stu-id="ae84c-108">Example 1: Create a management group</span></span>
```
PS C:\>New-AzureRmApiManagementGroup -Context $APImContext -Name "Group0001"
```

<span data-ttu-id="ae84c-109">Эта команда создает группу управления.</span><span class="sxs-lookup"><span data-stu-id="ae84c-109">This command creates a management group.</span></span>

## <span data-ttu-id="ae84c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ae84c-110">PARAMETERS</span></span>

### <span data-ttu-id="ae84c-111">-Context</span><span class="sxs-lookup"><span data-stu-id="ae84c-111">-Context</span></span>
<span data-ttu-id="ae84c-112">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="ae84c-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae84c-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="ae84c-113">-Description</span></span>
<span data-ttu-id="ae84c-114">Задает описание группы управления.</span><span class="sxs-lookup"><span data-stu-id="ae84c-114">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="ae84c-115">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="ae84c-115">-ExternalId</span></span>
<span data-ttu-id="ae84c-116">Для внешних групп это свойство включает идентификатор группы из внешнего поставщика удостоверений, например Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; в противном случае — значение null.</span><span class="sxs-lookup"><span data-stu-id="ae84c-116">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae84c-117">-GroupId</span><span class="sxs-lookup"><span data-stu-id="ae84c-117">-GroupId</span></span>
<span data-ttu-id="ae84c-118">Указывает идентификатор новой группы управления.</span><span class="sxs-lookup"><span data-stu-id="ae84c-118">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="ae84c-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ae84c-119">-Name</span></span>
<span data-ttu-id="ae84c-120">Указывает имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="ae84c-120">Specifies the management group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae84c-121">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="ae84c-121">-Type</span></span>
<span data-ttu-id="ae84c-122">Тип группы.</span><span class="sxs-lookup"><span data-stu-id="ae84c-122">Group Type.</span></span> <span data-ttu-id="ae84c-123">Пользовательская группа — это группа, определенная пользователем.</span><span class="sxs-lookup"><span data-stu-id="ae84c-123">Custom Group is User defined Group.</span></span> <span data-ttu-id="ae84c-124">В системную группу входят администраторы, разработчики и гости.</span><span class="sxs-lookup"><span data-stu-id="ae84c-124">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="ae84c-125">Вы не можете создать или обновить системную группу.</span><span class="sxs-lookup"><span data-stu-id="ae84c-125">You cannot create or update a System Group.</span></span>  <span data-ttu-id="ae84c-126">Внешняя группа — это группы из внешнего поставщика удостоверений, такие как Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ae84c-126">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="ae84c-127">Этот параметр является необязательным, и по умолчанию предполагается, что это настраиваемая группа.</span><span class="sxs-lookup"><span data-stu-id="ae84c-127">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae84c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae84c-128">-DefaultProfile</span></span>
<span data-ttu-id="ae84c-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ae84c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae84c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae84c-130">CommonParameters</span></span>
<span data-ttu-id="ae84c-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ae84c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae84c-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae84c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae84c-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ae84c-133">INPUTS</span></span>

## <span data-ttu-id="ae84c-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ae84c-134">OUTPUTS</span></span>

### <span data-ttu-id="ae84c-135">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ae84c-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="ae84c-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ae84c-136">NOTES</span></span>

## <span data-ttu-id="ae84c-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ae84c-137">RELATED LINKS</span></span>

[<span data-ttu-id="ae84c-138">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ae84c-138">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="ae84c-139">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ae84c-139">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="ae84c-140">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ae84c-140">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)



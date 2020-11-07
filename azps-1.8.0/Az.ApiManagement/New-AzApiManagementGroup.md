---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 22feec8308b682aa2290de6bd8b7361bb07cd560
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731672"
---
# <span data-ttu-id="80a95-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="80a95-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="80a95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="80a95-102">SYNOPSIS</span></span>
<span data-ttu-id="80a95-103">Создание группы управления API.</span><span class="sxs-lookup"><span data-stu-id="80a95-103">Creates an API management group.</span></span>

## <span data-ttu-id="80a95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="80a95-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="80a95-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80a95-105">DESCRIPTION</span></span>
<span data-ttu-id="80a95-106">Командлет **New-AzApiManagementGroup** создает группу управления API.</span><span class="sxs-lookup"><span data-stu-id="80a95-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="80a95-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="80a95-107">EXAMPLES</span></span>

### <span data-ttu-id="80a95-108">Пример 1: создание группы управления</span><span class="sxs-lookup"><span data-stu-id="80a95-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="80a95-109">Эта команда создает группу управления.</span><span class="sxs-lookup"><span data-stu-id="80a95-109">This command creates a management group.</span></span>

## <span data-ttu-id="80a95-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="80a95-110">PARAMETERS</span></span>

### <span data-ttu-id="80a95-111">-Context</span><span class="sxs-lookup"><span data-stu-id="80a95-111">-Context</span></span>
<span data-ttu-id="80a95-112">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="80a95-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="80a95-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80a95-113">-DefaultProfile</span></span>
<span data-ttu-id="80a95-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80a95-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80a95-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="80a95-115">-Description</span></span>
<span data-ttu-id="80a95-116">Задает описание группы управления.</span><span class="sxs-lookup"><span data-stu-id="80a95-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="80a95-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="80a95-117">-ExternalId</span></span>
<span data-ttu-id="80a95-118">Для внешних групп это свойство включает идентификатор группы из внешнего поставщика удостоверений, например Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; в противном случае — значение null.</span><span class="sxs-lookup"><span data-stu-id="80a95-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="80a95-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="80a95-119">-GroupId</span></span>
<span data-ttu-id="80a95-120">Указывает идентификатор новой группы управления.</span><span class="sxs-lookup"><span data-stu-id="80a95-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="80a95-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="80a95-121">-Name</span></span>
<span data-ttu-id="80a95-122">Указывает имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="80a95-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="80a95-123">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="80a95-123">-Type</span></span>
<span data-ttu-id="80a95-124">Тип группы.</span><span class="sxs-lookup"><span data-stu-id="80a95-124">Group Type.</span></span> <span data-ttu-id="80a95-125">Пользовательская группа — это группа, определенная пользователем.</span><span class="sxs-lookup"><span data-stu-id="80a95-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="80a95-126">В системную группу входят администраторы, разработчики и гости.</span><span class="sxs-lookup"><span data-stu-id="80a95-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="80a95-127">Вы не можете создать или обновить системную группу.</span><span class="sxs-lookup"><span data-stu-id="80a95-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="80a95-128">Внешняя группа — это группы из внешнего поставщика удостоверений, такие как Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="80a95-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="80a95-129">Этот параметр является необязательным, и по умолчанию предполагается, что это настраиваемая группа.</span><span class="sxs-lookup"><span data-stu-id="80a95-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType]
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System, External

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80a95-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80a95-130">CommonParameters</span></span>
<span data-ttu-id="80a95-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="80a95-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80a95-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="80a95-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80a95-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="80a95-133">INPUTS</span></span>

### <span data-ttu-id="80a95-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="80a95-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="80a95-135">System. String</span><span class="sxs-lookup"><span data-stu-id="80a95-135">System.String</span></span>

### <span data-ttu-id="80a95-136">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementGroupType, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="80a95-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="80a95-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="80a95-137">OUTPUTS</span></span>

### <span data-ttu-id="80a95-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="80a95-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="80a95-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="80a95-139">NOTES</span></span>

## <span data-ttu-id="80a95-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80a95-140">RELATED LINKS</span></span>

[<span data-ttu-id="80a95-141">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="80a95-141">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="80a95-142">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="80a95-142">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="80a95-143">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="80a95-143">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)



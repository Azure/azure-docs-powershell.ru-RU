---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGroup.md
ms.openlocfilehash: 8f7d221ca4f90f67bce038015b4c654881dfa598
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066709"
---
# <span data-ttu-id="1c227-101">New-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c227-101">New-AzApiManagementGroup</span></span>

## <span data-ttu-id="1c227-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1c227-102">SYNOPSIS</span></span>
<span data-ttu-id="1c227-103">Создание группы управления API.</span><span class="sxs-lookup"><span data-stu-id="1c227-103">Creates an API management group.</span></span>

## <span data-ttu-id="1c227-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1c227-104">SYNTAX</span></span>

```
New-AzApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c227-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c227-105">DESCRIPTION</span></span>
<span data-ttu-id="1c227-106">Командлет **New-AzApiManagementGroup** создает группу управления API.</span><span class="sxs-lookup"><span data-stu-id="1c227-106">The **New-AzApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="1c227-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1c227-107">EXAMPLES</span></span>

### <span data-ttu-id="1c227-108">Пример 1: создание группы управления</span><span class="sxs-lookup"><span data-stu-id="1c227-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="1c227-109">Эта команда создает группу управления.</span><span class="sxs-lookup"><span data-stu-id="1c227-109">This command creates a management group.</span></span>

## <span data-ttu-id="1c227-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1c227-110">PARAMETERS</span></span>

### <span data-ttu-id="1c227-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1c227-111">-Context</span></span>
<span data-ttu-id="1c227-112">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1c227-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c227-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c227-113">-DefaultProfile</span></span>
<span data-ttu-id="1c227-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c227-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c227-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="1c227-115">-Description</span></span>
<span data-ttu-id="1c227-116">Задает описание группы управления.</span><span class="sxs-lookup"><span data-stu-id="1c227-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="1c227-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="1c227-117">-ExternalId</span></span>
<span data-ttu-id="1c227-118">Для внешних групп это свойство включает идентификатор группы из внешнего поставщика удостоверений, например Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; в противном случае — значение null.</span><span class="sxs-lookup"><span data-stu-id="1c227-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

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

### <span data-ttu-id="1c227-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="1c227-119">-GroupId</span></span>
<span data-ttu-id="1c227-120">Указывает идентификатор новой группы управления.</span><span class="sxs-lookup"><span data-stu-id="1c227-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="1c227-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1c227-121">-Name</span></span>
<span data-ttu-id="1c227-122">Указывает имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="1c227-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="1c227-123">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="1c227-123">-Type</span></span>
<span data-ttu-id="1c227-124">Тип группы.</span><span class="sxs-lookup"><span data-stu-id="1c227-124">Group Type.</span></span> <span data-ttu-id="1c227-125">Пользовательская группа — это группа, определенная пользователем.</span><span class="sxs-lookup"><span data-stu-id="1c227-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="1c227-126">В системную группу входят администраторы, разработчики и гости.</span><span class="sxs-lookup"><span data-stu-id="1c227-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="1c227-127">Вы не можете создать или обновить системную группу.</span><span class="sxs-lookup"><span data-stu-id="1c227-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="1c227-128">Внешняя группа — это группы из внешнего поставщика удостоверений, такие как Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1c227-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="1c227-129">Этот параметр является необязательным, и по умолчанию предполагается, что это настраиваемая группа.</span><span class="sxs-lookup"><span data-stu-id="1c227-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

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

### <span data-ttu-id="1c227-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c227-130">CommonParameters</span></span>
<span data-ttu-id="1c227-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1c227-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c227-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c227-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c227-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1c227-133">INPUTS</span></span>

### <span data-ttu-id="1c227-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1c227-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1c227-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1c227-135">System.String</span></span>

### <span data-ttu-id="1c227-136">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. ServiceManagement.. PsApiManagementGroupType, Microsoft. Azure. PowerShell. командлеты. ApiManagement. ServiceManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="1c227-136">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroupType, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1c227-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c227-137">OUTPUTS</span></span>

### <span data-ttu-id="1c227-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c227-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="1c227-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="1c227-139">NOTES</span></span>

## <span data-ttu-id="1c227-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c227-140">RELATED LINKS</span></span>

[<span data-ttu-id="1c227-141">Get-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c227-141">Get-AzApiManagementGroup</span></span>](./Get-AzApiManagementGroup.md)

[<span data-ttu-id="1c227-142">Remove-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c227-142">Remove-AzApiManagementGroup</span></span>](./Remove-AzApiManagementGroup.md)

[<span data-ttu-id="1c227-143">Set-AzApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="1c227-143">Set-AzApiManagementGroup</span></span>](./Set-AzApiManagementGroup.md)



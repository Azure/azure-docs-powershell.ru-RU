---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: EE2BC1F7-E6F3-477D-8416-8E61893534E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementGroup.md
ms.openlocfilehash: 0443b9bc3ed2666600f2d119eca5b7173b21e89d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734198"
---
# <span data-ttu-id="54f61-101">New-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="54f61-101">New-AzureRmApiManagementGroup</span></span>

## <span data-ttu-id="54f61-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54f61-102">SYNOPSIS</span></span>
<span data-ttu-id="54f61-103">Создание группы управления API.</span><span class="sxs-lookup"><span data-stu-id="54f61-103">Creates an API management group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54f61-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54f61-104">SYNTAX</span></span>

```
New-AzureRmApiManagementGroup -Context <PsApiManagementContext> [-GroupId <String>] -Name <String>
 [-Description <String>] [-Type <PsApiManagementGroupType>] [-ExternalId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54f61-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54f61-105">DESCRIPTION</span></span>
<span data-ttu-id="54f61-106">Командлет **New-AzureRmApiManagementGroup** создает группу управления API.</span><span class="sxs-lookup"><span data-stu-id="54f61-106">The **New-AzureRmApiManagementGroup** cmdlet creates an API management group.</span></span>

## <span data-ttu-id="54f61-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54f61-107">EXAMPLES</span></span>

### <span data-ttu-id="54f61-108">Пример 1: создание группы управления</span><span class="sxs-lookup"><span data-stu-id="54f61-108">Example 1: Create a management group</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementGroup -Context $apimContext -Name "Group0001"
```

<span data-ttu-id="54f61-109">Эта команда создает группу управления.</span><span class="sxs-lookup"><span data-stu-id="54f61-109">This command creates a management group.</span></span>

## <span data-ttu-id="54f61-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54f61-110">PARAMETERS</span></span>

### <span data-ttu-id="54f61-111">-Context</span><span class="sxs-lookup"><span data-stu-id="54f61-111">-Context</span></span>
<span data-ttu-id="54f61-112">Задает экземпляр объекта **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="54f61-112">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f61-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f61-113">-DefaultProfile</span></span>
<span data-ttu-id="54f61-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54f61-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="54f61-115">-Описание</span><span class="sxs-lookup"><span data-stu-id="54f61-115">-Description</span></span>
<span data-ttu-id="54f61-116">Задает описание группы управления.</span><span class="sxs-lookup"><span data-stu-id="54f61-116">Specifies the description of the management group.</span></span>

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

### <span data-ttu-id="54f61-117">-ExternalId</span><span class="sxs-lookup"><span data-stu-id="54f61-117">-ExternalId</span></span>
<span data-ttu-id="54f61-118">Для внешних групп это свойство включает идентификатор группы из внешнего поставщика удостоверений, например Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; в противном случае — значение null.</span><span class="sxs-lookup"><span data-stu-id="54f61-118">For external groups, this property contains the id of the group from the external identity provider, e.g. Azure Active Directory aad://contoso5api.onmicrosoft.com/groups/12ad42b1-592f-4664-a77b4250-2f2e82579f4c; otherwise the value is null.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54f61-119">-GroupId</span><span class="sxs-lookup"><span data-stu-id="54f61-119">-GroupId</span></span>
<span data-ttu-id="54f61-120">Указывает идентификатор новой группы управления.</span><span class="sxs-lookup"><span data-stu-id="54f61-120">Specifies the identifier of the new management group.</span></span>

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

### <span data-ttu-id="54f61-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54f61-121">-Name</span></span>
<span data-ttu-id="54f61-122">Указывает имя группы управления.</span><span class="sxs-lookup"><span data-stu-id="54f61-122">Specifies the management group name.</span></span>

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

### <span data-ttu-id="54f61-123">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="54f61-123">-Type</span></span>
<span data-ttu-id="54f61-124">Тип группы.</span><span class="sxs-lookup"><span data-stu-id="54f61-124">Group Type.</span></span> <span data-ttu-id="54f61-125">Пользовательская группа — это группа, определенная пользователем.</span><span class="sxs-lookup"><span data-stu-id="54f61-125">Custom Group is User defined Group.</span></span> <span data-ttu-id="54f61-126">В системную группу входят администраторы, разработчики и гости.</span><span class="sxs-lookup"><span data-stu-id="54f61-126">System Group includes Administrator, Developers and Guests.</span></span> <span data-ttu-id="54f61-127">Вы не можете создать или обновить системную группу.</span><span class="sxs-lookup"><span data-stu-id="54f61-127">You cannot create or update a System Group.</span></span>  <span data-ttu-id="54f61-128">Внешняя группа — это группы из внешнего поставщика удостоверений, такие как Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54f61-128">External Group is groups from External Identity Provider like Azure Active Directory.</span></span> <span data-ttu-id="54f61-129">Этот параметр является необязательным, и по умолчанию предполагается, что это настраиваемая группа.</span><span class="sxs-lookup"><span data-stu-id="54f61-129">This parameter is optional and by default assumed to be a Custom Group.</span></span>

```yaml
Type: PsApiManagementGroupType
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f61-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f61-130">CommonParameters</span></span>
<span data-ttu-id="54f61-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54f61-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f61-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54f61-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f61-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54f61-133">INPUTS</span></span>

### <span data-ttu-id="54f61-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="54f61-134">None</span></span>
<span data-ttu-id="54f61-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="54f61-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="54f61-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54f61-136">OUTPUTS</span></span>

### <span data-ttu-id="54f61-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="54f61-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGroup</span></span>

## <span data-ttu-id="54f61-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="54f61-138">NOTES</span></span>

## <span data-ttu-id="54f61-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54f61-139">RELATED LINKS</span></span>

[<span data-ttu-id="54f61-140">Get-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="54f61-140">Get-AzureRmApiManagementGroup</span></span>](./Get-AzureRmApiManagementGroup.md)

[<span data-ttu-id="54f61-141">Remove-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="54f61-141">Remove-AzureRmApiManagementGroup</span></span>](./Remove-AzureRmApiManagementGroup.md)

[<span data-ttu-id="54f61-142">Set-AzureRmApiManagementGroup</span><span class="sxs-lookup"><span data-stu-id="54f61-142">Set-AzureRmApiManagementGroup</span></span>](./Set-AzureRmApiManagementGroup.md)



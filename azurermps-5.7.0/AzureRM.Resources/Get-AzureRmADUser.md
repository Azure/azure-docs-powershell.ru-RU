---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: e111da68e00e0edad54823c763c06f84ea5100e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733236"
---
# <span data-ttu-id="95257-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="95257-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="95257-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95257-102">SYNOPSIS</span></span>
<span data-ttu-id="95257-103">Фильтрует пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="95257-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95257-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95257-104">SYNTAX</span></span>

### <span data-ttu-id="95257-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95257-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95257-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="95257-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95257-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95257-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95257-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="95257-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95257-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="95257-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95257-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95257-110">DESCRIPTION</span></span>
<span data-ttu-id="95257-111">Фильтрует пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="95257-111">Filters active directory users.</span></span>

## <span data-ttu-id="95257-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95257-112">EXAMPLES</span></span>

### <span data-ttu-id="95257-113">Фильтрация пользователей, использующих UPN</span><span class="sxs-lookup"><span data-stu-id="95257-113">Filters users using UPN</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="95257-114">Получает пользователя с foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="95257-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="95257-115">Фильтрация пользователей с помощью строки поиска</span><span class="sxs-lookup"><span data-stu-id="95257-115">Filters users using Search String</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="95257-116">Фильтрует всех пользователей AD, у которых есть Joe в отображаемом имени.</span><span class="sxs-lookup"><span data-stu-id="95257-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="95257-117">Список пользователей рекламы</span><span class="sxs-lookup"><span data-stu-id="95257-117">List AD users</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="95257-118">Получает всех пользователей Active Directory</span><span class="sxs-lookup"><span data-stu-id="95257-118">Gets all AD users</span></span>

## <span data-ttu-id="95257-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95257-119">PARAMETERS</span></span>

### <span data-ttu-id="95257-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95257-120">-DefaultProfile</span></span>
<span data-ttu-id="95257-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="95257-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="95257-122">-Почта</span><span class="sxs-lookup"><span data-stu-id="95257-122">-Mail</span></span>
```yaml
Type: String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95257-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="95257-123">-ObjectId</span></span>
<span data-ttu-id="95257-124">Идентификатор объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="95257-124">Object id of the user.</span></span>

```yaml
Type: Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95257-125">-SearchString</span><span class="sxs-lookup"><span data-stu-id="95257-125">-SearchString</span></span>
<span data-ttu-id="95257-126">Отображаемое имя пользователя</span><span class="sxs-lookup"><span data-stu-id="95257-126">The user display name</span></span>

```yaml
Type: String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95257-127">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="95257-127">-UserPrincipalName</span></span>
<span data-ttu-id="95257-128">Имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="95257-128">UPN of the user.</span></span>

```yaml
Type: String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95257-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95257-129">CommonParameters</span></span>
<span data-ttu-id="95257-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95257-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95257-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95257-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95257-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95257-132">INPUTS</span></span>

### <span data-ttu-id="95257-133">Ничего</span><span class="sxs-lookup"><span data-stu-id="95257-133">None</span></span>
<span data-ttu-id="95257-134">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="95257-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95257-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95257-135">OUTPUTS</span></span>

### <span data-ttu-id="95257-136">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="95257-136">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="95257-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="95257-137">NOTES</span></span>

## <span data-ttu-id="95257-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95257-138">RELATED LINKS</span></span>

[<span data-ttu-id="95257-139">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="95257-139">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="95257-140">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="95257-140">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="95257-141">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="95257-141">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)


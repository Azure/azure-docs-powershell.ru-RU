---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADUser.md
ms.openlocfilehash: dd864d11608c33f758e0995d9dacf4afc454130a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559548"
---
# <span data-ttu-id="5326d-101">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5326d-101">Get-AzureRmADUser</span></span>

## <span data-ttu-id="5326d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5326d-102">SYNOPSIS</span></span>
<span data-ttu-id="5326d-103">Фильтрует пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5326d-103">Filters active directory users.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5326d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5326d-104">SYNTAX</span></span>

### <span data-ttu-id="5326d-105">EmptyParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5326d-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5326d-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="5326d-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADUser -SearchString <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5326d-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5326d-107">ObjectIdParameterSet</span></span>
```
Get-AzureRmADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5326d-108">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="5326d-108">UPNParameterSet</span></span>
```
Get-AzureRmADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5326d-109">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="5326d-109">MailParameterSet</span></span>
```
Get-AzureRmADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5326d-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5326d-110">DESCRIPTION</span></span>
<span data-ttu-id="5326d-111">Фильтрует пользователей Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5326d-111">Filters active directory users.</span></span>

## <span data-ttu-id="5326d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5326d-112">EXAMPLES</span></span>

### <span data-ttu-id="5326d-113">--------------------------Отфильтровывает пользователей, использующих UPN---------------------------</span><span class="sxs-lookup"><span data-stu-id="5326d-113">--------------------------  Filters users using UPN  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -UPN foo@domain.com
```

<span data-ttu-id="5326d-114">Получает пользователя с foo@domain.com</span><span class="sxs-lookup"><span data-stu-id="5326d-114">Gets user with foo@domain.com</span></span>

### <span data-ttu-id="5326d-115">--------------------------Отфильтровывает пользователей, использующих строку поиска--------------------------</span><span class="sxs-lookup"><span data-stu-id="5326d-115">--------------------------  Filters users using Search String  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser -SearchString Joe
```

<span data-ttu-id="5326d-116">Фильтрует всех пользователей AD, у которых есть Joe в отображаемом имени.</span><span class="sxs-lookup"><span data-stu-id="5326d-116">Filters all ad users that has Joe in the display name.</span></span>

### <span data-ttu-id="5326d-117">--------------------------"Пользователи рекламы в списке"--------------------------</span><span class="sxs-lookup"><span data-stu-id="5326d-117">--------------------------  List AD users  --------------------------</span></span>
```
PS C:\> Get-AzureRmADUser
```

<span data-ttu-id="5326d-118">Получает всех пользователей Active Directory</span><span class="sxs-lookup"><span data-stu-id="5326d-118">Gets all AD users</span></span>

## <span data-ttu-id="5326d-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5326d-119">PARAMETERS</span></span>

### <span data-ttu-id="5326d-120">-Почта</span><span class="sxs-lookup"><span data-stu-id="5326d-120">-Mail</span></span>
```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5326d-121">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5326d-121">-ObjectId</span></span>
<span data-ttu-id="5326d-122">Идентификатор объекта пользователя.</span><span class="sxs-lookup"><span data-stu-id="5326d-122">Object id of the user.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5326d-123">-SearchString</span><span class="sxs-lookup"><span data-stu-id="5326d-123">-SearchString</span></span>
<span data-ttu-id="5326d-124">Отображаемое имя пользователя</span><span class="sxs-lookup"><span data-stu-id="5326d-124">The user display name</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5326d-125">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5326d-125">-UserPrincipalName</span></span>
<span data-ttu-id="5326d-126">Имя участника-пользователя.</span><span class="sxs-lookup"><span data-stu-id="5326d-126">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5326d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5326d-127">-DefaultProfile</span></span>
<span data-ttu-id="5326d-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5326d-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5326d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5326d-129">CommonParameters</span></span>
<span data-ttu-id="5326d-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5326d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5326d-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5326d-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5326d-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5326d-132">INPUTS</span></span>

## <span data-ttu-id="5326d-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5326d-133">OUTPUTS</span></span>

### <span data-ttu-id="5326d-134">System. Collections. Generic. List ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser]</span><span class="sxs-lookup"><span data-stu-id="5326d-134">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser]</span></span>

## <span data-ttu-id="5326d-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="5326d-135">NOTES</span></span>

## <span data-ttu-id="5326d-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5326d-136">RELATED LINKS</span></span>

[<span data-ttu-id="5326d-137">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5326d-137">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="5326d-138">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5326d-138">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="5326d-139">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="5326d-139">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)


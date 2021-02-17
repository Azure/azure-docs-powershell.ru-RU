---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: c22643c4ce47fc59d2640a6dbbdf9c15b0846f98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100212924"
---
# <span data-ttu-id="9f673-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9f673-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="9f673-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f673-102">SYNOPSIS</span></span>
<span data-ttu-id="9f673-103">Извлекает список учетных данных, связанных с главой службы.</span><span class="sxs-lookup"><span data-stu-id="9f673-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="9f673-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9f673-104">SYNTAX</span></span>

### <span data-ttu-id="9f673-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f673-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f673-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f673-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9f673-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f673-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f673-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f673-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f673-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f673-109">DESCRIPTION</span></span>
<span data-ttu-id="9f673-110">Этот Get-AzADSpCredential можно использовать для извлечения списка учетных данных, связанных с главой службы.</span><span class="sxs-lookup"><span data-stu-id="9f673-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="9f673-111">Эта команда извлекает все свойства учетных данных (но не значения учетных данных), связанные с главой службы.</span><span class="sxs-lookup"><span data-stu-id="9f673-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="9f673-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9f673-112">EXAMPLES</span></span>

### <span data-ttu-id="9f673-113">Пример 1. Учетные данные списка по spn</span><span class="sxs-lookup"><span data-stu-id="9f673-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="9f673-114">Возвращает список учетных данных, связанных с главой службы с spN http://test12345 '.</span><span class="sxs-lookup"><span data-stu-id="9f673-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="9f673-115">Пример 2. Учетные данные списка по ид объекта</span><span class="sxs-lookup"><span data-stu-id="9f673-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="9f673-116">Возвращает список учетных данных, связанных с главой службы, с ид объекта "58e28616-99cc-4da4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="9f673-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="9f673-117">Пример 3. Учетные данные списка путем piping</span><span class="sxs-lookup"><span data-stu-id="9f673-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="9f673-118">Получает главную службу с ид объекта "58e28616-99cc-4da4-b705-7672130e1047" и передает ее в Get-AzADSpCredential-лист для списка всех учетных данных для этого основного обслуживания.</span><span class="sxs-lookup"><span data-stu-id="9f673-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="9f673-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f673-119">PARAMETERS</span></span>

### <span data-ttu-id="9f673-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f673-120">-DefaultProfile</span></span>
<span data-ttu-id="9f673-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9f673-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f673-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9f673-122">-DisplayName</span></span>
<span data-ttu-id="9f673-123">Отображаемая имя директора-службы</span><span class="sxs-lookup"><span data-stu-id="9f673-123">The display name of the service principal</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f673-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9f673-124">-ObjectId</span></span>
<span data-ttu-id="9f673-125">Object id of the service principal to retrieve credentials from.</span><span class="sxs-lookup"><span data-stu-id="9f673-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f673-126">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9f673-126">-ServicePrincipalName</span></span>
<span data-ttu-id="9f673-127">Имя (SPN) основной службы, из которого извлекались учетные данные.</span><span class="sxs-lookup"><span data-stu-id="9f673-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f673-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="9f673-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="9f673-129">Объект-служба, из который извлекает учетные данные.</span><span class="sxs-lookup"><span data-stu-id="9f673-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f673-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f673-130">CommonParameters</span></span>
<span data-ttu-id="9f673-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f673-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f673-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9f673-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f673-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f673-133">INPUTS</span></span>

### <span data-ttu-id="9f673-134">System.String</span><span class="sxs-lookup"><span data-stu-id="9f673-134">System.String</span></span>

### <span data-ttu-id="9f673-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9f673-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="9f673-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9f673-136">OUTPUTS</span></span>

### <span data-ttu-id="9f673-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="9f673-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="9f673-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9f673-138">NOTES</span></span>

## <span data-ttu-id="9f673-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f673-139">RELATED LINKS</span></span>

[<span data-ttu-id="9f673-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9f673-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="9f673-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9f673-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="9f673-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9f673-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)


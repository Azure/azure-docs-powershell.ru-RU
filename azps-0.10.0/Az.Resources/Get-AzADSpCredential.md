---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 40543468145c7fcfaf49fcfc7cad1cbf70938adf
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910962"
---
# <span data-ttu-id="e6afb-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e6afb-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="e6afb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6afb-102">SYNOPSIS</span></span>
<span data-ttu-id="e6afb-103">Извлекает список учетных данных, связанных с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="e6afb-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="e6afb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6afb-104">SYNTAX</span></span>

### <span data-ttu-id="e6afb-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6afb-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6afb-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6afb-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e6afb-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6afb-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6afb-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6afb-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6afb-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6afb-109">DESCRIPTION</span></span>
<span data-ttu-id="e6afb-110">Для получения списка учетных данных, связанных с субъектом-службой, можно использовать командлет Get-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="e6afb-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="e6afb-111">Эта команда извлекает все свойства учетных данных (но не значение учетных данных), связанные с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="e6afb-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="e6afb-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6afb-112">EXAMPLES</span></span>

### <span data-ttu-id="e6afb-113">Пример 1: список учетных данных по имени участника-службы</span><span class="sxs-lookup"><span data-stu-id="e6afb-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="e6afb-114">Возвращает список учетных данных, связанных с субъектом-службой с SPN " http://test12345 ".</span><span class="sxs-lookup"><span data-stu-id="e6afb-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="e6afb-115">Пример 2: перечисление учетных данных по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="e6afb-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="e6afb-116">Возвращает список учетных данных, связанных с субъектом-службой с идентификатором объекта "58e28616-99cc-4da4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="e6afb-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="e6afb-117">Пример 3: перечисление учетных данных по конвейеру</span><span class="sxs-lookup"><span data-stu-id="e6afb-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="e6afb-118">Возвращает субъекта-службы с идентификатором объекта "58e28616-99cc-4da4-b705-7672130e1047" и добавляет его в командлет Get-AzADSpCredential, чтобы получить список всех учетных данных для этого субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="e6afb-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="e6afb-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6afb-119">PARAMETERS</span></span>

### <span data-ttu-id="e6afb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6afb-120">-DefaultProfile</span></span>
<span data-ttu-id="e6afb-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e6afb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6afb-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e6afb-122">-DisplayName</span></span>
<span data-ttu-id="e6afb-123">Отображаемое имя субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="e6afb-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="e6afb-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e6afb-124">-ObjectId</span></span>
<span data-ttu-id="e6afb-125">Идентификатор объекта субъекта-службы, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e6afb-125">The object id of the service principal to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6afb-126">-Намерено</span><span class="sxs-lookup"><span data-stu-id="e6afb-126">-ServicePrincipalName</span></span>
<span data-ttu-id="e6afb-127">Имя (SPN) субъекта-службы, из которого нужно получить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e6afb-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="e6afb-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="e6afb-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="e6afb-129">Объект субъекта-службы, из которого требуется получить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="e6afb-129">The service principal object to retrieve the credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: SPNObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6afb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6afb-130">CommonParameters</span></span>
<span data-ttu-id="e6afb-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6afb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6afb-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6afb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6afb-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6afb-133">INPUTS</span></span>

### <span data-ttu-id="e6afb-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e6afb-134">System.Guid</span></span>

### <span data-ttu-id="e6afb-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e6afb-135">System.String</span></span>

### <span data-ttu-id="e6afb-136">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e6afb-136">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="e6afb-137">Параметры: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e6afb-137">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="e6afb-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6afb-138">OUTPUTS</span></span>

### <span data-ttu-id="e6afb-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="e6afb-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="e6afb-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6afb-140">NOTES</span></span>

## <span data-ttu-id="e6afb-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6afb-141">RELATED LINKS</span></span>

[<span data-ttu-id="e6afb-142">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e6afb-142">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="e6afb-143">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="e6afb-143">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="e6afb-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e6afb-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)


---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadspcredential
schema: 2.0.0
ms.openlocfilehash: a0f4c41b310e820b939500b8496b411d7b0266d1
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913997"
---
# <span data-ttu-id="2ccac-101">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2ccac-101">Get-AzureRmADSpCredential</span></span>

## <span data-ttu-id="2ccac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ccac-102">SYNOPSIS</span></span>
<span data-ttu-id="2ccac-103">Извлекает список учетных данных, связанных с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="2ccac-103">Retrieves a list of credentials associated with a service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2ccac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ccac-104">SYNTAX</span></span>

### <span data-ttu-id="2ccac-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ccac-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADSpCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ccac-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ccac-106">SPNParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2ccac-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ccac-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ccac-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ccac-108">SPNObjectParameterSet</span></span>
```
Get-AzureRmADSpCredential -ServicePrincipalObject <PSADServicePrincipal>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ccac-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ccac-109">DESCRIPTION</span></span>
<span data-ttu-id="2ccac-110">Для получения списка учетных данных, связанных с субъектом-службой, можно использовать командлет Get-AzureRmADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="2ccac-110">The Get-AzureRmADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="2ccac-111">Эта команда извлекает все свойства учетных данных (но не значение учетных данных), связанные с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="2ccac-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="2ccac-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ccac-112">EXAMPLES</span></span>

### <span data-ttu-id="2ccac-113">Пример 1: список учетных данных по имени участника-службы</span><span class="sxs-lookup"><span data-stu-id="2ccac-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="2ccac-114">Возвращает список учетных данных, связанных с субъектом-службой с SPN " http://test12345 ".</span><span class="sxs-lookup"><span data-stu-id="2ccac-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="2ccac-115">Пример 2: перечисление учетных данных по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="2ccac-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzureRmADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="2ccac-116">Возвращает список учетных данных, связанных с субъектом-службой с идентификатором объекта "58e28616-99cc-4da4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="2ccac-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="2ccac-117">Пример 3: перечисление учетных данных по конвейеру</span><span class="sxs-lookup"><span data-stu-id="2ccac-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzureRmADSpCredential
```

<span data-ttu-id="2ccac-118">Возвращает субъекта-службы с идентификатором объекта "58e28616-99cc-4da4-b705-7672130e1047" и добавляет его в командлет Get-AzureRmADSpCredential, чтобы получить список всех учетных данных для этого субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="2ccac-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzureRmADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="2ccac-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ccac-119">PARAMETERS</span></span>

### <span data-ttu-id="2ccac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ccac-120">-DefaultProfile</span></span>
<span data-ttu-id="2ccac-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2ccac-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2ccac-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2ccac-122">-DisplayName</span></span>
<span data-ttu-id="2ccac-123">Отображаемое имя субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="2ccac-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="2ccac-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2ccac-124">-ObjectId</span></span>
<span data-ttu-id="2ccac-125">Идентификатор объекта субъекта-службы, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="2ccac-125">The object id of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="2ccac-126">-Намерено</span><span class="sxs-lookup"><span data-stu-id="2ccac-126">-ServicePrincipalName</span></span>
<span data-ttu-id="2ccac-127">Имя (SPN) субъекта-службы, из которого нужно получить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="2ccac-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="2ccac-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="2ccac-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="2ccac-129">Объект субъекта-службы, из которого требуется получить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="2ccac-129">The service principal object to retrieve the credentials from.</span></span>

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

### <span data-ttu-id="2ccac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ccac-130">CommonParameters</span></span>
<span data-ttu-id="2ccac-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ccac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ccac-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ccac-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ccac-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ccac-133">INPUTS</span></span>

### <span data-ttu-id="2ccac-134">System. GUID</span><span class="sxs-lookup"><span data-stu-id="2ccac-134">System.Guid</span></span>

### <span data-ttu-id="2ccac-135">System. String</span><span class="sxs-lookup"><span data-stu-id="2ccac-135">System.String</span></span>

### <span data-ttu-id="2ccac-136">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2ccac-136">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="2ccac-137">Параметры: ServicePrincipalObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2ccac-137">Parameters: ServicePrincipalObject (ByValue)</span></span>

## <span data-ttu-id="2ccac-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ccac-138">OUTPUTS</span></span>

### <span data-ttu-id="2ccac-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="2ccac-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="2ccac-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ccac-140">NOTES</span></span>

## <span data-ttu-id="2ccac-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ccac-141">RELATED LINKS</span></span>

[<span data-ttu-id="2ccac-142">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2ccac-142">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="2ccac-143">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="2ccac-143">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="2ccac-144">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="2ccac-144">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)


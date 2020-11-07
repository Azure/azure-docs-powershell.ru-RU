---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7690143F-5F09-4739-9F66-B2ACDF8305F4
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADSpCredential.md
ms.openlocfilehash: 5307e070f8c568473e1ce35f1183517cd3def05c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729449"
---
# <span data-ttu-id="14c77-101">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="14c77-101">Get-AzADSpCredential</span></span>

## <span data-ttu-id="14c77-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="14c77-102">SYNOPSIS</span></span>
<span data-ttu-id="14c77-103">Извлекает список учетных данных, связанных с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="14c77-103">Retrieves a list of credentials associated with a service principal.</span></span>

## <span data-ttu-id="14c77-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="14c77-104">SYNTAX</span></span>

### <span data-ttu-id="14c77-105">ObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="14c77-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADSpCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c77-106">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c77-106">SPNParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14c77-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c77-107">DisplayNameParameterSet</span></span>
```
Get-AzADSpCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14c77-108">SPNObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14c77-108">SPNObjectParameterSet</span></span>
```
Get-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="14c77-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="14c77-109">DESCRIPTION</span></span>
<span data-ttu-id="14c77-110">Для получения списка учетных данных, связанных с субъектом-службой, можно использовать командлет Get-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="14c77-110">The Get-AzADSpCredential cmdlet can be used to retrieve a list of credentials associated with a service principal.</span></span>
<span data-ttu-id="14c77-111">Эта команда извлекает все свойства учетных данных (но не значение учетных данных), связанные с субъектом-службой.</span><span class="sxs-lookup"><span data-stu-id="14c77-111">This command will retrieve all of the credential properties (but not the credential value) associated with the service principal.</span></span>

## <span data-ttu-id="14c77-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="14c77-112">EXAMPLES</span></span>

### <span data-ttu-id="14c77-113">Пример 1: список учетных данных по имени участника-службы</span><span class="sxs-lookup"><span data-stu-id="14c77-113">Example 1 - List credentials by SPN</span></span>

```
PS C:\> Get-AzADSpCredential -ServicePrincipalName http://test12345
```

<span data-ttu-id="14c77-114">Возвращает список учетных данных, связанных с субъектом-службой с SPN " http://test12345 ".</span><span class="sxs-lookup"><span data-stu-id="14c77-114">Returns a list of credentials associated with the service principal with SPN 'http://test12345'.</span></span>

### <span data-ttu-id="14c77-115">Пример 2: перечисление учетных данных по идентификатору объекта</span><span class="sxs-lookup"><span data-stu-id="14c77-115">Example 2 - List credentials by object id</span></span>

```
PS C:\> Get-AzADSpCredential -ObjectId 58e28616-99cc-4da4-b705-7672130e1047
```

<span data-ttu-id="14c77-116">Возвращает список учетных данных, связанных с субъектом-службой с идентификатором объекта "58e28616-99cc-4da4-b705-7672130e1047".</span><span class="sxs-lookup"><span data-stu-id="14c77-116">Returns a list of credentials associated with the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047".</span></span>

### <span data-ttu-id="14c77-117">Пример 3: перечисление учетных данных по конвейеру</span><span class="sxs-lookup"><span data-stu-id="14c77-117">Example 3 - List credentials by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 58e28616-99cc-4da4-b705-7672130e1047 | Get-AzADSpCredential
```

<span data-ttu-id="14c77-118">Возвращает субъекта-службы с идентификатором объекта "58e28616-99cc-4da4-b705-7672130e1047" и добавляет его в командлет Get-AzADSpCredential, чтобы получить список всех учетных данных для этого субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="14c77-118">Gets the service principal with object id "58e28616-99cc-4da4-b705-7672130e1047" and pipes it to the Get-AzADSpCredential cmdlet to list all credentials for that service principal.</span></span>

## <span data-ttu-id="14c77-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="14c77-119">PARAMETERS</span></span>

### <span data-ttu-id="14c77-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14c77-120">-DefaultProfile</span></span>
<span data-ttu-id="14c77-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="14c77-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="14c77-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="14c77-122">-DisplayName</span></span>
<span data-ttu-id="14c77-123">Отображаемое имя субъекта-службы</span><span class="sxs-lookup"><span data-stu-id="14c77-123">The display name of the service principal</span></span>

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

### <span data-ttu-id="14c77-124">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="14c77-124">-ObjectId</span></span>
<span data-ttu-id="14c77-125">Идентификатор объекта субъекта-службы, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="14c77-125">The object id of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="14c77-126">-Намерено</span><span class="sxs-lookup"><span data-stu-id="14c77-126">-ServicePrincipalName</span></span>
<span data-ttu-id="14c77-127">Имя (SPN) субъекта-службы, из которого нужно получить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="14c77-127">The name (SPN) of the service principal to retrieve credentials from.</span></span>

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

### <span data-ttu-id="14c77-128">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="14c77-128">-ServicePrincipalObject</span></span>
<span data-ttu-id="14c77-129">Объект субъекта-службы, из которого требуется получить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="14c77-129">The service principal object to retrieve the credentials from.</span></span>

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

### <span data-ttu-id="14c77-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14c77-130">CommonParameters</span></span>
<span data-ttu-id="14c77-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="14c77-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14c77-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14c77-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14c77-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="14c77-133">INPUTS</span></span>

### <span data-ttu-id="14c77-134">System. String</span><span class="sxs-lookup"><span data-stu-id="14c77-134">System.String</span></span>

### <span data-ttu-id="14c77-135">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="14c77-135">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="14c77-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="14c77-136">OUTPUTS</span></span>

### <span data-ttu-id="14c77-137">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="14c77-137">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="14c77-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="14c77-138">NOTES</span></span>

## <span data-ttu-id="14c77-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="14c77-139">RELATED LINKS</span></span>

[<span data-ttu-id="14c77-140">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="14c77-140">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="14c77-141">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="14c77-141">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="14c77-142">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="14c77-142">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)


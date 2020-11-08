---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: 7bfa908e83d7731ca2ed5613d82f42b19c392b2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236645"
---
# <span data-ttu-id="8591f-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8591f-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="8591f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8591f-102">SYNOPSIS</span></span>
<span data-ttu-id="8591f-103">Извлекает список учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="8591f-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="8591f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8591f-104">SYNTAX</span></span>

### <span data-ttu-id="8591f-105">ApplicationObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8591f-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8591f-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8591f-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8591f-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8591f-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8591f-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8591f-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8591f-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8591f-109">DESCRIPTION</span></span>
<span data-ttu-id="8591f-110">Командлет Get-AzADAppCredential можно использовать для получения списка учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="8591f-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="8591f-111">Эта команда извлекает все свойства учетных данных (но не значение учетных данных), связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="8591f-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="8591f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8591f-112">EXAMPLES</span></span>

### <span data-ttu-id="8591f-113">Пример 1: получение учетных данных приложения с помощью идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="8591f-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="8591f-114">Возвращает список учетных данных, связанных с приложением с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="8591f-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="8591f-115">Пример 2: получение учетных данных приложения с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="8591f-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="8591f-116">Возвращает приложение с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476" и преобразует его в командлет Get-AzADAppCredential, чтобы получить список всех учетных данных для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="8591f-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="8591f-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8591f-117">PARAMETERS</span></span>

### <span data-ttu-id="8591f-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8591f-118">-ApplicationId</span></span>
<span data-ttu-id="8591f-119">Идентификатор приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="8591f-119">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8591f-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="8591f-120">-ApplicationObject</span></span>
<span data-ttu-id="8591f-121">Объект приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="8591f-121">The application object to retrieve credentials from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8591f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8591f-122">-DefaultProfile</span></span>
<span data-ttu-id="8591f-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8591f-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8591f-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8591f-124">-DisplayName</span></span>
<span data-ttu-id="8591f-125">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="8591f-125">The display name of the application.</span></span>

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

### <span data-ttu-id="8591f-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="8591f-126">-ObjectId</span></span>
<span data-ttu-id="8591f-127">Идентификатор объекта приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="8591f-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8591f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8591f-128">CommonParameters</span></span>
<span data-ttu-id="8591f-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8591f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8591f-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8591f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8591f-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8591f-131">INPUTS</span></span>

### <span data-ttu-id="8591f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8591f-132">System.String</span></span>

### <span data-ttu-id="8591f-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="8591f-133">System.Guid</span></span>

### <span data-ttu-id="8591f-134">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="8591f-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="8591f-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8591f-135">OUTPUTS</span></span>

### <span data-ttu-id="8591f-136">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="8591f-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="8591f-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="8591f-137">NOTES</span></span>

## <span data-ttu-id="8591f-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8591f-138">RELATED LINKS</span></span>

[<span data-ttu-id="8591f-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8591f-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="8591f-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8591f-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="8591f-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8591f-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: fdef07255316b1d7529202c36b844e8732c76390
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729464"
---
# <span data-ttu-id="d9687-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d9687-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="d9687-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d9687-102">SYNOPSIS</span></span>
<span data-ttu-id="d9687-103">Извлекает список учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="d9687-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="d9687-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d9687-104">SYNTAX</span></span>

### <span data-ttu-id="d9687-105">ApplicationObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d9687-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9687-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9687-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9687-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9687-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9687-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9687-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d9687-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9687-109">DESCRIPTION</span></span>
<span data-ttu-id="d9687-110">Командлет Get-AzADAppCredential можно использовать для получения списка учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="d9687-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="d9687-111">Эта команда извлекает все свойства учетных данных (но не значение учетных данных), связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="d9687-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="d9687-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d9687-112">EXAMPLES</span></span>

### <span data-ttu-id="d9687-113">Пример 1. получение учетных данных приложения с помощью идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="d9687-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="d9687-114">Возвращает список учетных данных, связанных с приложением с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="d9687-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="d9687-115">Пример 2: получение учетных данных приложения с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="d9687-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="d9687-116">Возвращает приложение с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476" и преобразует его в командлет Get-AzADAppCredential, чтобы получить список всех учетных данных для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="d9687-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="d9687-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d9687-117">PARAMETERS</span></span>

### <span data-ttu-id="d9687-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d9687-118">-ApplicationId</span></span>
<span data-ttu-id="d9687-119">Идентификатор приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d9687-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="d9687-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="d9687-120">-ApplicationObject</span></span>
<span data-ttu-id="d9687-121">Объект приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d9687-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="d9687-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9687-122">-DefaultProfile</span></span>
<span data-ttu-id="d9687-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d9687-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9687-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d9687-124">-DisplayName</span></span>
<span data-ttu-id="d9687-125">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="d9687-125">The display name of the application.</span></span>

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

### <span data-ttu-id="d9687-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d9687-126">-ObjectId</span></span>
<span data-ttu-id="d9687-127">Идентификатор объекта приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="d9687-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="d9687-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9687-128">CommonParameters</span></span>
<span data-ttu-id="d9687-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d9687-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9687-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9687-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9687-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d9687-131">INPUTS</span></span>

### <span data-ttu-id="d9687-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d9687-132">System.String</span></span>

### <span data-ttu-id="d9687-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d9687-133">System.Guid</span></span>

### <span data-ttu-id="d9687-134">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d9687-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="d9687-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d9687-135">OUTPUTS</span></span>

### <span data-ttu-id="d9687-136">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="d9687-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="d9687-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="d9687-137">NOTES</span></span>

## <span data-ttu-id="d9687-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d9687-138">RELATED LINKS</span></span>

[<span data-ttu-id="d9687-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d9687-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="d9687-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d9687-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="d9687-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d9687-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)


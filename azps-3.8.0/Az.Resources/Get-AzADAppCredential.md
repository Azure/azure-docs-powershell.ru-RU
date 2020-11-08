---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: ef03850e2a8c0981ad4a1b642df51c1fec462513
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066499"
---
# <span data-ttu-id="df5a8-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="df5a8-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="df5a8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="df5a8-103">Извлекает список учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="df5a8-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="df5a8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df5a8-104">SYNTAX</span></span>

### <span data-ttu-id="df5a8-105">ApplicationObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df5a8-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df5a8-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="df5a8-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df5a8-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="df5a8-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="df5a8-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df5a8-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df5a8-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df5a8-109">DESCRIPTION</span></span>
<span data-ttu-id="df5a8-110">Командлет Get-AzADAppCredential можно использовать для получения списка учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="df5a8-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="df5a8-111">Эта команда извлекает все свойства учетных данных (но не значение учетных данных), связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="df5a8-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="df5a8-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df5a8-112">EXAMPLES</span></span>

### <span data-ttu-id="df5a8-113">Пример 1. получение учетных данных приложения с помощью идентификатора объекта</span><span class="sxs-lookup"><span data-stu-id="df5a8-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="df5a8-114">Возвращает список учетных данных, связанных с приложением с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="df5a8-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="df5a8-115">Пример 2: получение учетных данных приложения с помощью трубопроводов</span><span class="sxs-lookup"><span data-stu-id="df5a8-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="df5a8-116">Возвращает приложение с идентификатором объекта "1f99cf81-0146-4f4e-beae-2007d0668476" и преобразует его в командлет Get-AzADAppCredential, чтобы получить список всех учетных данных для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="df5a8-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="df5a8-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df5a8-117">PARAMETERS</span></span>

### <span data-ttu-id="df5a8-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="df5a8-118">-ApplicationId</span></span>
<span data-ttu-id="df5a8-119">Идентификатор приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="df5a8-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="df5a8-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="df5a8-120">-ApplicationObject</span></span>
<span data-ttu-id="df5a8-121">Объект приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="df5a8-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="df5a8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df5a8-122">-DefaultProfile</span></span>
<span data-ttu-id="df5a8-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="df5a8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df5a8-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="df5a8-124">-DisplayName</span></span>
<span data-ttu-id="df5a8-125">Отображаемое имя приложения.</span><span class="sxs-lookup"><span data-stu-id="df5a8-125">The display name of the application.</span></span>

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

### <span data-ttu-id="df5a8-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="df5a8-126">-ObjectId</span></span>
<span data-ttu-id="df5a8-127">Идентификатор объекта приложения, из которого извлекаются учетные данные.</span><span class="sxs-lookup"><span data-stu-id="df5a8-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="df5a8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df5a8-128">CommonParameters</span></span>
<span data-ttu-id="df5a8-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df5a8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df5a8-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="df5a8-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df5a8-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df5a8-131">INPUTS</span></span>

### <span data-ttu-id="df5a8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="df5a8-132">System.String</span></span>

### <span data-ttu-id="df5a8-133">System. GUID</span><span class="sxs-lookup"><span data-stu-id="df5a8-133">System.Guid</span></span>

### <span data-ttu-id="df5a8-134">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="df5a8-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="df5a8-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df5a8-135">OUTPUTS</span></span>

### <span data-ttu-id="df5a8-136">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="df5a8-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="df5a8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="df5a8-137">NOTES</span></span>

## <span data-ttu-id="df5a8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df5a8-138">RELATED LINKS</span></span>

[<span data-ttu-id="df5a8-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="df5a8-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="df5a8-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="df5a8-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="df5a8-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="df5a8-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)


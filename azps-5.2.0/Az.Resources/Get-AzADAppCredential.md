---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: 7bfa908e83d7731ca2ed5613d82f42b19c392b2f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98395391"
---
# <span data-ttu-id="158a7-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="158a7-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="158a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="158a7-102">SYNOPSIS</span></span>
<span data-ttu-id="158a7-103">Извлекает список учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="158a7-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="158a7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="158a7-104">SYNTAX</span></span>

### <span data-ttu-id="158a7-105">ApplicationObjectIdParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="158a7-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="158a7-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="158a7-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="158a7-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="158a7-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="158a7-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="158a7-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="158a7-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="158a7-109">DESCRIPTION</span></span>
<span data-ttu-id="158a7-110">Этот Get-AzADAppCredential можно использовать для получения списка учетных данных, связанных с приложением.</span><span class="sxs-lookup"><span data-stu-id="158a7-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="158a7-111">Эта команда извлекает все свойства учетных данных (но не значения учетных данных), связанные с приложением.</span><span class="sxs-lookup"><span data-stu-id="158a7-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="158a7-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="158a7-112">EXAMPLES</span></span>

### <span data-ttu-id="158a7-113">Пример 1. Получение учетных данных приложения по ид объекта</span><span class="sxs-lookup"><span data-stu-id="158a7-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="158a7-114">Возвращает список учетных данных, связанных с приложением, которое имеет object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span><span class="sxs-lookup"><span data-stu-id="158a7-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="158a7-115">Пример 2. Получение учетных данных приложения путем piping</span><span class="sxs-lookup"><span data-stu-id="158a7-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="158a7-116">Получает приложение с ид объекта "1f99cf81-0146-4f4e-beae-2007d0668476" и передает его в Get-AzADAppCredential-лист, чтобы получить все учетные данные для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="158a7-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="158a7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="158a7-117">PARAMETERS</span></span>

### <span data-ttu-id="158a7-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="158a7-118">-ApplicationId</span></span>
<span data-ttu-id="158a7-119">ID приложения для получения учетных данных.</span><span class="sxs-lookup"><span data-stu-id="158a7-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="158a7-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="158a7-120">-ApplicationObject</span></span>
<span data-ttu-id="158a7-121">Объект приложения, из который нужно получить учетные данные.</span><span class="sxs-lookup"><span data-stu-id="158a7-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="158a7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158a7-122">-DefaultProfile</span></span>
<span data-ttu-id="158a7-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="158a7-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="158a7-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="158a7-124">-DisplayName</span></span>
<span data-ttu-id="158a7-125">Отображаемого имени приложения.</span><span class="sxs-lookup"><span data-stu-id="158a7-125">The display name of the application.</span></span>

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

### <span data-ttu-id="158a7-126">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="158a7-126">-ObjectId</span></span>
<span data-ttu-id="158a7-127">ИД объекта приложения для получения учетных данных.</span><span class="sxs-lookup"><span data-stu-id="158a7-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="158a7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158a7-128">CommonParameters</span></span>
<span data-ttu-id="158a7-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="158a7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158a7-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="158a7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158a7-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="158a7-131">INPUTS</span></span>

### <span data-ttu-id="158a7-132">System.String</span><span class="sxs-lookup"><span data-stu-id="158a7-132">System.String</span></span>

### <span data-ttu-id="158a7-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="158a7-133">System.Guid</span></span>

### <span data-ttu-id="158a7-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="158a7-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="158a7-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="158a7-135">OUTPUTS</span></span>

### <span data-ttu-id="158a7-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="158a7-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="158a7-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="158a7-137">NOTES</span></span>

## <span data-ttu-id="158a7-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="158a7-138">RELATED LINKS</span></span>

[<span data-ttu-id="158a7-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="158a7-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="158a7-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="158a7-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="158a7-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="158a7-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)


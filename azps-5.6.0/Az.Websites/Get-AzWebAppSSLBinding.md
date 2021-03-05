---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: 08a9fbd9798a3fd3b53d7d71aca9ebd607d23164
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973699"
---
# <span data-ttu-id="237ac-101">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="237ac-101">Get-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="237ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="237ac-102">SYNOPSIS</span></span>
<span data-ttu-id="237ac-103">Получает SSL-привязку SSL сертификата Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="237ac-103">Gets an Azure Web App certificate SSL binding.</span></span>

## <span data-ttu-id="237ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="237ac-104">SYNTAX</span></span>

### <span data-ttu-id="237ac-105">S1</span><span class="sxs-lookup"><span data-stu-id="237ac-105">S1</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="237ac-106">S2</span><span class="sxs-lookup"><span data-stu-id="237ac-106">S2</span></span>
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="237ac-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="237ac-107">DESCRIPTION</span></span>
<span data-ttu-id="237ac-108">Для Azure Web App с помощью **cmdlet Get-AzWebAppSSLBinding** обеспечивается привязка SSL для Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="237ac-108">The **Get-AzWebAppSSLBinding** cmdlet gets a Secure Sockets Layer (SSL) binding for an Azure Web App.</span></span>
<span data-ttu-id="237ac-109">Привязки SSL используются для связывания Веб-приложения с загруженным сертификатом.</span><span class="sxs-lookup"><span data-stu-id="237ac-109">SSL bindings are used to associate a Web App with an uploaded certificate.</span></span>
<span data-ttu-id="237ac-110">Веб-приложения можно привязыть к нескольким сертификатам.</span><span class="sxs-lookup"><span data-stu-id="237ac-110">Web Apps can be bound to multiple certificates.</span></span>

## <span data-ttu-id="237ac-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="237ac-111">EXAMPLES</span></span>

### <span data-ttu-id="237ac-112">Пример 1. Получить привязки SSL для веб-приложения</span><span class="sxs-lookup"><span data-stu-id="237ac-112">Example 1: Get SSL bindings for a Web App</span></span>
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

<span data-ttu-id="237ac-113">Эта команда извлекает привязки SSL для веб-приложения ContosoWebApp, связанного с группой ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="237ac-113">This command retrieves the SSL bindings for the Web App ContosoWebApp, which is associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="237ac-114">Пример 2. Использование ссылки на объект для получения привязки SSL для веб-приложения</span><span class="sxs-lookup"><span data-stu-id="237ac-114">Example 2: Use an object reference to get SSL bindings for a Web App</span></span>
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

<span data-ttu-id="237ac-115">Команды в этом примере также получают привязки SSL для Web App ContosoWebApp; Но в этом случае вместо имени веб-приложения и связанной группы ресурсов используется ссылка на объект.</span><span class="sxs-lookup"><span data-stu-id="237ac-115">The commands in this example also get the SSL bindings for the Web App ContosoWebApp; in this case, however, an object reference is used instead of the Web App name and the name of the associated resource group.</span></span>
<span data-ttu-id="237ac-116">Эта ссылка создается первой командой в примере, которая использует **Get-AzWebApp** для создания ссылки на объект с именем ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="237ac-116">This object reference is created by the first command in the example, which uses **Get-AzWebApp** to create an object reference to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="237ac-117">Эта ссылка на объект хранится в переменной с именем $WebApp.</span><span class="sxs-lookup"><span data-stu-id="237ac-117">That object reference is stored in a variable named $WebApp.</span></span>
<span data-ttu-id="237ac-118">Эта переменная и командлет **Get-AzWebAppSSLBinding** используются второй командой для получения привязки SSL.</span><span class="sxs-lookup"><span data-stu-id="237ac-118">This variable, and the **Get-AzWebAppSSLBinding** cmdlet, are then used by the second command to get the SSL bindings.</span></span>

## <span data-ttu-id="237ac-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="237ac-119">PARAMETERS</span></span>

### <span data-ttu-id="237ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="237ac-120">-DefaultProfile</span></span>
<span data-ttu-id="237ac-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="237ac-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="237ac-122">-Name</span><span class="sxs-lookup"><span data-stu-id="237ac-122">-Name</span></span>
<span data-ttu-id="237ac-123">Имя привязки SSL.</span><span class="sxs-lookup"><span data-stu-id="237ac-123">Specifies the name of the SSL binding.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="237ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="237ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="237ac-125">Имя группы ресурсов, которая назначена сертификату.</span><span class="sxs-lookup"><span data-stu-id="237ac-125">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="237ac-126">В одной команде нельзя использовать параметр *ResourceGroupName* и *параметр WebApp.*</span><span class="sxs-lookup"><span data-stu-id="237ac-126">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="237ac-127">-Slot</span><span class="sxs-lookup"><span data-stu-id="237ac-127">-Slot</span></span>
<span data-ttu-id="237ac-128">Указывает слот развертывания Web App.</span><span class="sxs-lookup"><span data-stu-id="237ac-128">Specifies a Web App deployment slot.</span></span>
<span data-ttu-id="237ac-129">Чтобы получить слот развертывания, используйте Get-AzWebAppSlot управления.</span><span class="sxs-lookup"><span data-stu-id="237ac-129">To get a deployment slot, use the Get-AzWebAppSlot cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="237ac-130">-WebApp</span><span class="sxs-lookup"><span data-stu-id="237ac-130">-WebApp</span></span>
<span data-ttu-id="237ac-131">Определяет веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="237ac-131">Specifies a Web App.</span></span>
<span data-ttu-id="237ac-132">Чтобы получить веб-приложение, воспользуйтесь Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="237ac-132">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="237ac-133">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="237ac-133">-WebAppName</span></span>
<span data-ttu-id="237ac-134">Указывает имя веб-приложения, из которого этот cmdlet получает привязки SSL.</span><span class="sxs-lookup"><span data-stu-id="237ac-134">Specifies the name of the Web App that this cmdlet gets SSL bindings from.</span></span>
<span data-ttu-id="237ac-135">В одной команде нельзя использовать *параметры WebAppName* и *WebApp.*</span><span class="sxs-lookup"><span data-stu-id="237ac-135">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="237ac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="237ac-136">CommonParameters</span></span>
<span data-ttu-id="237ac-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="237ac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="237ac-138">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="237ac-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="237ac-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="237ac-139">INPUTS</span></span>

### <span data-ttu-id="237ac-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="237ac-140">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="237ac-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="237ac-141">OUTPUTS</span></span>

### <span data-ttu-id="237ac-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="237ac-142">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="237ac-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="237ac-143">NOTES</span></span>

## <span data-ttu-id="237ac-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="237ac-144">RELATED LINKS</span></span>

[<span data-ttu-id="237ac-145">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="237ac-145">New-AzWebAppSSLBinding</span></span>](./New-AzWebAppSSLBinding.md)

[<span data-ttu-id="237ac-146">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="237ac-146">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="237ac-147">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="237ac-147">Get-AzWebApp</span></span>](./Get-AzWebApp.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-AzWebAppCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppCertificate.md
ms.openlocfilehash: 56f8d69325e5a7918668ac2807449f348e73c91b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100216516"
---
# <span data-ttu-id="7222a-101">New-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="7222a-101">New-AzWebAppCertificate</span></span>

## <span data-ttu-id="7222a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7222a-102">SYNOPSIS</span></span>
<span data-ttu-id="7222a-103">Создает сертификат, управляемый службой приложений для Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="7222a-103">Creates an App service managed certificate for an Azure Web App.</span></span> 

## <span data-ttu-id="7222a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7222a-104">SYNTAX</span></span>

```
New-AzWebAppCertificate [-ResourceGroupName] <String> [-WebAppName] <String> [-Name] <String> [[-Slot] <String>]
 [-HostName] <String> [-AddBinding] [[-SslState] <SslState>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7222a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7222a-105">DESCRIPTION</span></span>
<span data-ttu-id="7222a-106">**Новый-AzWebAppCertificate** создает управляемый сертификат Azure App Service Managed Certificate.</span><span class="sxs-lookup"><span data-stu-id="7222a-106">The **New-AzWebAppCertificate** cmdlet creates an Azure App Service Managed Certificate</span></span>
## <span data-ttu-id="7222a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7222a-107">EXAMPLES</span></span>

### <span data-ttu-id="7222a-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7222a-108">Example 1</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net"
```

<span data-ttu-id="7222a-109">Эта команда создает сертификат App Service Managed для данного веб-приложения</span><span class="sxs-lookup"><span data-stu-id="7222a-109">This command create an App Service Managed Certificate for the given WebApp</span></span>

### <span data-ttu-id="7222a-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="7222a-110">Example 2</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -Slot "test" -AddCertBinding
```

<span data-ttu-id="7222a-111">Эта команда создает сертификат, управляемый службой App Service, и связывает его с данным слотом WebApp.</span><span class="sxs-lookup"><span data-stu-id="7222a-111">This command create an App Service Managed Certificate and binds to the given WebApp Slot.</span></span>

### <span data-ttu-id="7222a-112">Пример 3</span><span class="sxs-lookup"><span data-stu-id="7222a-112">Example 3</span></span>
```powershell
PS C:\> New-AzWebAppCertificate -ResourceGroupName Default-Web-WestUS -WebAppName "ContosoSite" -Name"ContosoCert" -HostName "www.ContosoSite.net" -AddBinding
```

<span data-ttu-id="7222a-113">Эта команда создает сертификат, управляемый службой App Service, и связывает его с данным webApp.</span><span class="sxs-lookup"><span data-stu-id="7222a-113">This command create an App Service Managed Certificate and binds to the given WebApp.</span></span>

## <span data-ttu-id="7222a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7222a-114">PARAMETERS</span></span>

### <span data-ttu-id="7222a-115">-AddBinding</span><span class="sxs-lookup"><span data-stu-id="7222a-115">-AddBinding</span></span>
<span data-ttu-id="7222a-116">Чтобы добавить созданный сертификат в webApp/slot.</span><span class="sxs-lookup"><span data-stu-id="7222a-116">To add the created certificate to WebApp/slot.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7222a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7222a-117">-DefaultProfile</span></span>
<span data-ttu-id="7222a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7222a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7222a-119">-HostName</span><span class="sxs-lookup"><span data-stu-id="7222a-119">-HostName</span></span>
<span data-ttu-id="7222a-120">Пользовательские имена сайтов, связанные с веб-приложением или слотом.</span><span class="sxs-lookup"><span data-stu-id="7222a-120">Custom hostnames associated with web app/slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7222a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7222a-121">-Name</span></span>
<span data-ttu-id="7222a-122">Имя сертификата.</span><span class="sxs-lookup"><span data-stu-id="7222a-122">The name of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7222a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7222a-123">-ResourceGroupName</span></span>
<span data-ttu-id="7222a-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7222a-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7222a-125">-Slot</span><span class="sxs-lookup"><span data-stu-id="7222a-125">-Slot</span></span>
<span data-ttu-id="7222a-126">Название слота веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="7222a-126">The name of the web app slot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7222a-127">-SslState</span><span class="sxs-lookup"><span data-stu-id="7222a-127">-SslState</span></span>
<span data-ttu-id="7222a-128">Параметр состояния SSL.</span><span class="sxs-lookup"><span data-stu-id="7222a-128">Ssl state option.</span></span>
<span data-ttu-id="7222a-129">Используйте "SniEnabled" или "IpBasedEnabled".</span><span class="sxs-lookup"><span data-stu-id="7222a-129">Use either 'SniEnabled' or 'IpBasedEnabled'.</span></span>
<span data-ttu-id="7222a-130">По умолчанию этот параметр имеет значение "SniEnabled".</span><span class="sxs-lookup"><span data-stu-id="7222a-130">Default option is 'SniEnabled'.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7222a-131">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="7222a-131">-WebAppName</span></span>
<span data-ttu-id="7222a-132">Имя веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="7222a-132">The name of the web app.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7222a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7222a-133">CommonParameters</span></span>
<span data-ttu-id="7222a-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7222a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7222a-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7222a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7222a-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7222a-136">INPUTS</span></span>

### <span data-ttu-id="7222a-137">Нет</span><span class="sxs-lookup"><span data-stu-id="7222a-137">None</span></span>

## <span data-ttu-id="7222a-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7222a-138">OUTPUTS</span></span>

### <span data-ttu-id="7222a-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="7222a-139">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="7222a-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7222a-140">NOTES</span></span>

## <span data-ttu-id="7222a-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7222a-141">RELATED LINKS</span></span>
[<span data-ttu-id="7222a-142">Remove-AzWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="7222a-142">Remove-AzWebAppCertificate</span></span>](./Remove-AzWebAppCertificate.md)
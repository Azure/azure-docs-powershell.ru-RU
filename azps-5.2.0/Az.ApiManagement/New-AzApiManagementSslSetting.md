---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408463"
---
# <span data-ttu-id="e98b5-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="e98b5-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="e98b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e98b5-102">SYNOPSIS</span></span>
<span data-ttu-id="e98b5-103">Создание экземпляра PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="e98b5-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="e98b5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e98b5-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e98b5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e98b5-105">DESCRIPTION</span></span>
<span data-ttu-id="e98b5-106">Команда-помощник для создания экземпляра PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="e98b5-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="e98b5-107">Эта команда будет использоваться с командой New-AzApiManagement команды.</span><span class="sxs-lookup"><span data-stu-id="e98b5-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="e98b5-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e98b5-108">EXAMPLES</span></span>

### <span data-ttu-id="e98b5-109">Пример 1. Создание параметра SSL для установки TLS 1.0 как в области backend, так и в frontend</span><span class="sxs-lookup"><span data-stu-id="e98b5-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="e98b5-110">Создайте новый экземпляр PsApiManagementSlSetting, чтобы включить TLSv 1.0 в frontend (между клиентом и APIM) и Backend (между APIM и Backend) шлюза ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="e98b5-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="e98b5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e98b5-111">PARAMETERS</span></span>

### <span data-ttu-id="e98b5-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="e98b5-112">-BackendProtocol</span></span>
<span data-ttu-id="e98b5-113">Параметры протокола backend Security.</span><span class="sxs-lookup"><span data-stu-id="e98b5-113">Backend Security protocol settings.</span></span> <span data-ttu-id="e98b5-114">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e98b5-114">This parameter is optional.</span></span>
<span data-ttu-id="e98b5-115">Допустимые параметры `Tls11` протокола: Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="e98b5-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98b5-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="e98b5-116">-CipherSuite</span></span>
<span data-ttu-id="e98b5-117">Параметры наборов шифров (SSL) в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="e98b5-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="e98b5-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e98b5-118">This parameter is optional.</span></span>
<span data-ttu-id="e98b5-119">Допустимые `TripleDes168` параметры: Enable /Disable Tripe Des 168</span><span class="sxs-lookup"><span data-stu-id="e98b5-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98b5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e98b5-120">-DefaultProfile</span></span>
<span data-ttu-id="e98b5-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e98b5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e98b5-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="e98b5-122">-FrontendProtocol</span></span>
<span data-ttu-id="e98b5-123">Параметры протокола frontend Security.</span><span class="sxs-lookup"><span data-stu-id="e98b5-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="e98b5-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e98b5-124">This parameter is optional.</span></span>
<span data-ttu-id="e98b5-125">Допустимые параметры `Tls11` протокола: Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="e98b5-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98b5-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="e98b5-126">-ServerProtocol</span></span>
<span data-ttu-id="e98b5-127">Параметры протокола сервера, например Http2.</span><span class="sxs-lookup"><span data-stu-id="e98b5-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="e98b5-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="e98b5-128">This parameter is optional.</span></span>
<span data-ttu-id="e98b5-129">Допустимые `Http2` параметры: включить http 2.0</span><span class="sxs-lookup"><span data-stu-id="e98b5-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e98b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e98b5-130">CommonParameters</span></span>
<span data-ttu-id="e98b5-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e98b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e98b5-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e98b5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e98b5-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e98b5-133">INPUTS</span></span>

### <span data-ttu-id="e98b5-134">Нет</span><span class="sxs-lookup"><span data-stu-id="e98b5-134">None</span></span>

## <span data-ttu-id="e98b5-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e98b5-135">OUTPUTS</span></span>

### <span data-ttu-id="e98b5-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="e98b5-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="e98b5-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e98b5-137">NOTES</span></span>

## <span data-ttu-id="e98b5-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e98b5-138">RELATED LINKS</span></span>

[<span data-ttu-id="e98b5-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="e98b5-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)


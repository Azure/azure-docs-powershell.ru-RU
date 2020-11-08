---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243765"
---
# <span data-ttu-id="30083-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="30083-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="30083-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="30083-102">SYNOPSIS</span></span>
<span data-ttu-id="30083-103">Создает экземпляр класса PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="30083-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="30083-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="30083-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="30083-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="30083-105">DESCRIPTION</span></span>
<span data-ttu-id="30083-106">Вспомогательная команда для создания экземпляра PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="30083-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="30083-107">Эта команда используется с New-AzApiManagement командой.</span><span class="sxs-lookup"><span data-stu-id="30083-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="30083-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="30083-108">EXAMPLES</span></span>

### <span data-ttu-id="30083-109">Пример 1: Создание параметра SSL для включения TLS 1,0 на внутреннем и внешнем интерфейсе</span><span class="sxs-lookup"><span data-stu-id="30083-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="30083-110">Создайте новый экземпляр PsApiManagementSslSetting для включения TLSv 1,0 на обоих интерфейсах (между клиентом и APIM) и внутреннего сервера (между APIM и внутренним) и серверным интерфейсом ApiManagement шлюза.</span><span class="sxs-lookup"><span data-stu-id="30083-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="30083-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="30083-111">PARAMETERS</span></span>

### <span data-ttu-id="30083-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="30083-112">-BackendProtocol</span></span>
<span data-ttu-id="30083-113">Внутренние параметры протокола безопасности.</span><span class="sxs-lookup"><span data-stu-id="30083-113">Backend Security protocol settings.</span></span> <span data-ttu-id="30083-114">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="30083-114">This parameter is optional.</span></span>
<span data-ttu-id="30083-115">Допустимые параметры протокола: `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="30083-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="30083-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="30083-116">-CipherSuite</span></span>
<span data-ttu-id="30083-117">Параметры комплектов шифров SSL в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="30083-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="30083-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="30083-118">This parameter is optional.</span></span>
<span data-ttu-id="30083-119">Допустимые параметры `TripleDes168` — Включение и отключение обработки данных Des 168</span><span class="sxs-lookup"><span data-stu-id="30083-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="30083-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30083-120">-DefaultProfile</span></span>
<span data-ttu-id="30083-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="30083-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="30083-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="30083-122">-FrontendProtocol</span></span>
<span data-ttu-id="30083-123">Параметры протоколов безопасности переднего плана.</span><span class="sxs-lookup"><span data-stu-id="30083-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="30083-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="30083-124">This parameter is optional.</span></span>
<span data-ttu-id="30083-125">Допустимые параметры протокола: `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="30083-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="30083-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="30083-126">-ServerProtocol</span></span>
<span data-ttu-id="30083-127">Параметры протокола сервера, например Http2.</span><span class="sxs-lookup"><span data-stu-id="30083-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="30083-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="30083-128">This parameter is optional.</span></span>
<span data-ttu-id="30083-129">Допустимые параметры: `Http2` -Enable Http 2,0</span><span class="sxs-lookup"><span data-stu-id="30083-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="30083-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30083-130">CommonParameters</span></span>
<span data-ttu-id="30083-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="30083-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30083-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30083-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30083-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="30083-133">INPUTS</span></span>

### <span data-ttu-id="30083-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="30083-134">None</span></span>

## <span data-ttu-id="30083-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="30083-135">OUTPUTS</span></span>

### <span data-ttu-id="30083-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="30083-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="30083-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="30083-137">NOTES</span></span>

## <span data-ttu-id="30083-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="30083-138">RELATED LINKS</span></span>

[<span data-ttu-id="30083-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="30083-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)


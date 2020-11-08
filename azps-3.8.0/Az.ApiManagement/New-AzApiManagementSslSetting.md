---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 709e8483a5f21e3afc58add1046b5dae22bea7b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066679"
---
# <span data-ttu-id="5cefe-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="5cefe-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="5cefe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5cefe-102">SYNOPSIS</span></span>
<span data-ttu-id="5cefe-103">Создает экземпляр класса PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="5cefe-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="5cefe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5cefe-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5cefe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cefe-105">DESCRIPTION</span></span>
<span data-ttu-id="5cefe-106">Вспомогательная команда для создания экземпляра PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="5cefe-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="5cefe-107">Эта команда используется с New-AzApiManagement командой.</span><span class="sxs-lookup"><span data-stu-id="5cefe-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="5cefe-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5cefe-108">EXAMPLES</span></span>

### <span data-ttu-id="5cefe-109">Пример 1: Создание параметра SSL для включения TLS 1,0 на внутреннем и внешнем интерфейсе</span><span class="sxs-lookup"><span data-stu-id="5cefe-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="5cefe-110">Создайте новый экземпляр PsApiManagementSslSetting для включения TLSv 1,0 на обоих интерфейсах (между клиентом и APIM) и внутреннего сервера (между APIM и внутренним) и серверным интерфейсом ApiManagement шлюза.</span><span class="sxs-lookup"><span data-stu-id="5cefe-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="5cefe-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5cefe-111">PARAMETERS</span></span>

### <span data-ttu-id="5cefe-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="5cefe-112">-BackendProtocol</span></span>
<span data-ttu-id="5cefe-113">Внутренние параметры протокола безопасности.</span><span class="sxs-lookup"><span data-stu-id="5cefe-113">Backend Security protocol settings.</span></span> <span data-ttu-id="5cefe-114">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5cefe-114">This parameter is optional.</span></span>
<span data-ttu-id="5cefe-115">Допустимые параметры протокола: `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="5cefe-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="5cefe-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="5cefe-116">-CipherSuite</span></span>
<span data-ttu-id="5cefe-117">Параметры комплектов шифров SSL в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="5cefe-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="5cefe-118">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5cefe-118">This parameter is optional.</span></span>
<span data-ttu-id="5cefe-119">Допустимые параметры `TripleDes168` — Включение и отключение обработки данных Des 168</span><span class="sxs-lookup"><span data-stu-id="5cefe-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="5cefe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cefe-120">-DefaultProfile</span></span>
<span data-ttu-id="5cefe-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5cefe-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cefe-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="5cefe-122">-FrontendProtocol</span></span>
<span data-ttu-id="5cefe-123">Параметры протоколов безопасности переднего плана.</span><span class="sxs-lookup"><span data-stu-id="5cefe-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="5cefe-124">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5cefe-124">This parameter is optional.</span></span>
<span data-ttu-id="5cefe-125">Допустимые параметры протокола: `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="5cefe-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="5cefe-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="5cefe-126">-ServerProtocol</span></span>
<span data-ttu-id="5cefe-127">Параметры протокола сервера, например Http2.</span><span class="sxs-lookup"><span data-stu-id="5cefe-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="5cefe-128">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="5cefe-128">This parameter is optional.</span></span>
<span data-ttu-id="5cefe-129">Допустимые параметры: `Http2` -Enable Http 2,0</span><span class="sxs-lookup"><span data-stu-id="5cefe-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="5cefe-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cefe-130">CommonParameters</span></span>
<span data-ttu-id="5cefe-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5cefe-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cefe-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5cefe-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cefe-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5cefe-133">INPUTS</span></span>

### <span data-ttu-id="5cefe-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="5cefe-134">None</span></span>

## <span data-ttu-id="5cefe-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5cefe-135">OUTPUTS</span></span>

### <span data-ttu-id="5cefe-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="5cefe-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="5cefe-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5cefe-137">NOTES</span></span>

## <span data-ttu-id="5cefe-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5cefe-138">RELATED LINKS</span></span>

[<span data-ttu-id="5cefe-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5cefe-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)


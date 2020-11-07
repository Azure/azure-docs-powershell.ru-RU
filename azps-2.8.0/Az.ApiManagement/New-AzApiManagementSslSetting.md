---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 7c4fb7c2147d7daf3307c2895893198ebe805ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728023"
---
# <span data-ttu-id="9ca99-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="9ca99-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="9ca99-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ca99-102">SYNOPSIS</span></span>
<span data-ttu-id="9ca99-103">Создает экземпляр класса PsApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="9ca99-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="9ca99-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ca99-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ca99-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ca99-105">DESCRIPTION</span></span>
<span data-ttu-id="9ca99-106">Вспомогательная команда для создания экземпляра PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="9ca99-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="9ca99-107">Эта команда используется с New-AzApiManagement командой.</span><span class="sxs-lookup"><span data-stu-id="9ca99-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="9ca99-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ca99-108">EXAMPLES</span></span>

### <span data-ttu-id="9ca99-109">Пример 1: Создание параметра SSL для включения TLS 1,0 на внутреннем и внешнем интерфейсе</span><span class="sxs-lookup"><span data-stu-id="9ca99-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="9ca99-110">Создайте новый экземпляр PsApiManagementSslSetting для включения TLSv 1,0 на обоих интерфейсах (между клиентом и APIM) и внутреннего сервера (между APIM и внутренним) и серверным интерфейсом ApiManagement шлюза.</span><span class="sxs-lookup"><span data-stu-id="9ca99-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="9ca99-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ca99-111">PARAMETERS</span></span>

### <span data-ttu-id="9ca99-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="9ca99-112">-BackendProtocol</span></span>
<span data-ttu-id="9ca99-113">Внутренние параметры протокола безопасности.</span><span class="sxs-lookup"><span data-stu-id="9ca99-113">Backend Security protocol settings.</span></span> <span data-ttu-id="9ca99-114">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9ca99-114">This parameter is optional.</span></span>

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

### <span data-ttu-id="9ca99-115">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="9ca99-115">-CipherSuite</span></span>
<span data-ttu-id="9ca99-116">Параметры комплектов шифров SSL в указанном порядке.</span><span class="sxs-lookup"><span data-stu-id="9ca99-116">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="9ca99-117">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9ca99-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="9ca99-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ca99-118">-DefaultProfile</span></span>
<span data-ttu-id="9ca99-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ca99-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ca99-120">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="9ca99-120">-FrontendProtocol</span></span>
<span data-ttu-id="9ca99-121">Параметры протоколов безопасности переднего плана.</span><span class="sxs-lookup"><span data-stu-id="9ca99-121">Frontend Security protocols settings.</span></span> <span data-ttu-id="9ca99-122">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9ca99-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="9ca99-123">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="9ca99-123">-ServerProtocol</span></span>
<span data-ttu-id="9ca99-124">Параметры протокола сервера, например Http2.</span><span class="sxs-lookup"><span data-stu-id="9ca99-124">Server protocol settings like Http2.</span></span> <span data-ttu-id="9ca99-125">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9ca99-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="9ca99-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ca99-126">CommonParameters</span></span>
<span data-ttu-id="9ca99-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ca99-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ca99-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ca99-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ca99-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ca99-129">INPUTS</span></span>

### <span data-ttu-id="9ca99-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="9ca99-130">None</span></span>

## <span data-ttu-id="9ca99-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ca99-131">OUTPUTS</span></span>

### <span data-ttu-id="9ca99-132">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="9ca99-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="9ca99-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ca99-133">NOTES</span></span>

## <span data-ttu-id="9ca99-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ca99-134">RELATED LINKS</span></span>

[<span data-ttu-id="9ca99-135">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9ca99-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)


---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 52d40ed69adda157a8fdacd9d6c961f88508fbb9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720156"
---
# <span data-ttu-id="64efd-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="64efd-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="64efd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="64efd-102">SYNOPSIS</span></span>
<span data-ttu-id="64efd-103">Возвращает сертификаты управления API, настроенные для взаимной проверки подлинности с помощью внутреннего сервера в службе.</span><span class="sxs-lookup"><span data-stu-id="64efd-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="64efd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="64efd-104">SYNTAX</span></span>

### <span data-ttu-id="64efd-105">GetAllCertificates (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="64efd-105">GetAllCertificates (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64efd-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="64efd-106">GetByCertificateId</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64efd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="64efd-107">DESCRIPTION</span></span>
<span data-ttu-id="64efd-108">Командлет **Get-AzApiManagementCertificate** получает все указанные вами сертификаты управления API Azure или сертификаты.</span><span class="sxs-lookup"><span data-stu-id="64efd-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="64efd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="64efd-109">EXAMPLES</span></span>

### <span data-ttu-id="64efd-110">Пример 1: получение всех сертификатов</span><span class="sxs-lookup"><span data-stu-id="64efd-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="64efd-111">Эта команда получает все сертификаты управления API.</span><span class="sxs-lookup"><span data-stu-id="64efd-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="64efd-112">Пример 2: получение сертификата с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="64efd-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="64efd-113">Эта команда получает сертификат управления API с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="64efd-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="64efd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="64efd-114">PARAMETERS</span></span>

### <span data-ttu-id="64efd-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="64efd-115">-CertificateId</span></span>
<span data-ttu-id="64efd-116">Указывает идентификатор получаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="64efd-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCertificateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64efd-117">-Context</span><span class="sxs-lookup"><span data-stu-id="64efd-117">-Context</span></span>
<span data-ttu-id="64efd-118">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="64efd-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64efd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64efd-119">-DefaultProfile</span></span>
<span data-ttu-id="64efd-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="64efd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64efd-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="64efd-121">-Confirm</span></span>
<span data-ttu-id="64efd-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="64efd-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64efd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64efd-123">-WhatIf</span></span>
<span data-ttu-id="64efd-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="64efd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64efd-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="64efd-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64efd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64efd-126">CommonParameters</span></span>
<span data-ttu-id="64efd-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="64efd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64efd-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64efd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64efd-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="64efd-129">INPUTS</span></span>

### <span data-ttu-id="64efd-130">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="64efd-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="64efd-131">System. String</span><span class="sxs-lookup"><span data-stu-id="64efd-131">System.String</span></span>

## <span data-ttu-id="64efd-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="64efd-132">OUTPUTS</span></span>

### <span data-ttu-id="64efd-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="64efd-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="64efd-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="64efd-134">NOTES</span></span>

## <span data-ttu-id="64efd-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="64efd-135">RELATED LINKS</span></span>

[<span data-ttu-id="64efd-136">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="64efd-136">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="64efd-137">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="64efd-137">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="64efd-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="64efd-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)



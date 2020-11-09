---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 9826de76a65fe097d2daba106bd74df5e94a730e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244648"
---
# <span data-ttu-id="75229-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="75229-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="75229-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75229-102">SYNOPSIS</span></span>
<span data-ttu-id="75229-103">Возвращает сертификаты управления API, настроенные для взаимной проверки подлинности с помощью внутреннего сервера в службе.</span><span class="sxs-lookup"><span data-stu-id="75229-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="75229-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75229-104">SYNTAX</span></span>

### <span data-ttu-id="75229-105">ContextParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75229-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="75229-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="75229-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75229-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75229-107">DESCRIPTION</span></span>
<span data-ttu-id="75229-108">Командлет **Get-AzApiManagementCertificate** получает все указанные вами сертификаты управления API Azure или сертификаты.</span><span class="sxs-lookup"><span data-stu-id="75229-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="75229-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75229-109">EXAMPLES</span></span>

### <span data-ttu-id="75229-110">Пример 1: получение всех сертификатов</span><span class="sxs-lookup"><span data-stu-id="75229-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="75229-111">Эта команда получает все сертификаты управления API.</span><span class="sxs-lookup"><span data-stu-id="75229-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="75229-112">Пример 2: получение сертификата с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="75229-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="75229-113">Эта команда получает сертификат управления API с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="75229-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="75229-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75229-114">PARAMETERS</span></span>

### <span data-ttu-id="75229-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="75229-115">-CertificateId</span></span>
<span data-ttu-id="75229-116">Указывает идентификатор получаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="75229-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75229-117">-Context</span><span class="sxs-lookup"><span data-stu-id="75229-117">-Context</span></span>
<span data-ttu-id="75229-118">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="75229-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75229-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75229-119">-DefaultProfile</span></span>
<span data-ttu-id="75229-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75229-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75229-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75229-121">-ResourceId</span></span>
<span data-ttu-id="75229-122">Идентификатор ресурса ARM сертификата.</span><span class="sxs-lookup"><span data-stu-id="75229-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="75229-123">Если задано значение, это попытается найти сертификат по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="75229-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="75229-124">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="75229-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75229-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75229-125">-Confirm</span></span>
<span data-ttu-id="75229-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75229-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75229-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75229-127">-WhatIf</span></span>
<span data-ttu-id="75229-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75229-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75229-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75229-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75229-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75229-130">CommonParameters</span></span>
<span data-ttu-id="75229-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75229-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75229-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75229-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75229-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75229-133">INPUTS</span></span>

### <span data-ttu-id="75229-134">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="75229-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="75229-135">System. String</span><span class="sxs-lookup"><span data-stu-id="75229-135">System.String</span></span>

## <span data-ttu-id="75229-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75229-136">OUTPUTS</span></span>

### <span data-ttu-id="75229-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="75229-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="75229-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="75229-138">NOTES</span></span>

## <span data-ttu-id="75229-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75229-139">RELATED LINKS</span></span>

[<span data-ttu-id="75229-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="75229-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="75229-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="75229-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="75229-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="75229-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


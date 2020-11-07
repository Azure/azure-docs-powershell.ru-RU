---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: b6825d23244664b475dbd28472dc30f33117a59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733287"
---
# <span data-ttu-id="eafcd-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="eafcd-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="eafcd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eafcd-102">SYNOPSIS</span></span>
<span data-ttu-id="eafcd-103">Возвращает сертификаты управления API, настроенные для взаимной проверки подлинности с помощью внутреннего сервера в службе.</span><span class="sxs-lookup"><span data-stu-id="eafcd-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eafcd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eafcd-104">SYNTAX</span></span>

### <span data-ttu-id="eafcd-105">GetAllCertificates (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="eafcd-105">GetAllCertificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eafcd-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="eafcd-106">GetByCertificateId</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eafcd-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eafcd-107">DESCRIPTION</span></span>
<span data-ttu-id="eafcd-108">Командлет **Get-AzureRmApiManagementCertificate** получает все указанные вами сертификаты управления API Azure или сертификаты.</span><span class="sxs-lookup"><span data-stu-id="eafcd-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="eafcd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eafcd-109">EXAMPLES</span></span>

### <span data-ttu-id="eafcd-110">Пример 1: получение всех сертификатов</span><span class="sxs-lookup"><span data-stu-id="eafcd-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="eafcd-111">Эта команда получает все сертификаты управления API.</span><span class="sxs-lookup"><span data-stu-id="eafcd-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="eafcd-112">Пример 2: получение сертификата с помощью идентификатора</span><span class="sxs-lookup"><span data-stu-id="eafcd-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="eafcd-113">Эта команда получает сертификат управления API с указанным ИДЕНТИФИКАТОРом.</span><span class="sxs-lookup"><span data-stu-id="eafcd-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="eafcd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eafcd-114">PARAMETERS</span></span>

### <span data-ttu-id="eafcd-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="eafcd-115">-CertificateId</span></span>
<span data-ttu-id="eafcd-116">Указывает идентификатор получаемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="eafcd-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByCertificateId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eafcd-117">-Context</span><span class="sxs-lookup"><span data-stu-id="eafcd-117">-Context</span></span>
<span data-ttu-id="eafcd-118">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="eafcd-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eafcd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eafcd-119">-DefaultProfile</span></span>
<span data-ttu-id="eafcd-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eafcd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafcd-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eafcd-121">-Confirm</span></span>
<span data-ttu-id="eafcd-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="eafcd-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafcd-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eafcd-123">-WhatIf</span></span>
<span data-ttu-id="eafcd-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="eafcd-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eafcd-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="eafcd-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eafcd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eafcd-126">CommonParameters</span></span>
<span data-ttu-id="eafcd-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eafcd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eafcd-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eafcd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eafcd-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eafcd-129">INPUTS</span></span>

### <span data-ttu-id="eafcd-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="eafcd-130">None</span></span>
<span data-ttu-id="eafcd-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="eafcd-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="eafcd-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eafcd-132">OUTPUTS</span></span>

### <span data-ttu-id="eafcd-133">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="eafcd-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="eafcd-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="eafcd-134">NOTES</span></span>

## <span data-ttu-id="eafcd-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eafcd-135">RELATED LINKS</span></span>

[<span data-ttu-id="eafcd-136">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="eafcd-136">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="eafcd-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="eafcd-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="eafcd-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="eafcd-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)



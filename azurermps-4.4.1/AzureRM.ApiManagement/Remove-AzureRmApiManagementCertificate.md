---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 5844bbfd59e38691a28720d5cab4e73e334af88d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732284"
---
# <span data-ttu-id="1f638-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1f638-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="1f638-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1f638-102">SYNOPSIS</span></span>
<span data-ttu-id="1f638-103">Удаляет сертификат управления API.</span><span class="sxs-lookup"><span data-stu-id="1f638-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f638-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1f638-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f638-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f638-105">DESCRIPTION</span></span>
<span data-ttu-id="1f638-106">Командлет **Remove-AzureRmApiManagementCertificate** Удаляет сертификат управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="1f638-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="1f638-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1f638-107">EXAMPLES</span></span>

### <span data-ttu-id="1f638-108">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="1f638-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="1f638-109">Эта команда удаляет указанный сертификат управления API.</span><span class="sxs-lookup"><span data-stu-id="1f638-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="1f638-110">Так как указан параметр *Force* , подтверждение не требуется.</span><span class="sxs-lookup"><span data-stu-id="1f638-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="1f638-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1f638-111">PARAMETERS</span></span>

### <span data-ttu-id="1f638-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="1f638-112">-CertificateId</span></span>
<span data-ttu-id="1f638-113">Указывает ИД сертификата, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="1f638-113">Specifies the ID of the certificate to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f638-114">-Context</span><span class="sxs-lookup"><span data-stu-id="1f638-114">-Context</span></span>
<span data-ttu-id="1f638-115">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1f638-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1f638-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1f638-116">-PassThru</span></span>
<span data-ttu-id="1f638-117">PassThru</span><span class="sxs-lookup"><span data-stu-id="1f638-117">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f638-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f638-118">-Confirm</span></span>
<span data-ttu-id="1f638-119">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1f638-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f638-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f638-120">-WhatIf</span></span>
<span data-ttu-id="1f638-121">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1f638-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f638-122">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1f638-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f638-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f638-123">-DefaultProfile</span></span>
<span data-ttu-id="1f638-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1f638-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f638-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f638-125">CommonParameters</span></span>
<span data-ttu-id="1f638-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1f638-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f638-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f638-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f638-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1f638-128">INPUTS</span></span>

## <span data-ttu-id="1f638-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1f638-129">OUTPUTS</span></span>

### <span data-ttu-id="1f638-130">Значением</span><span class="sxs-lookup"><span data-stu-id="1f638-130">Boolean</span></span>

## <span data-ttu-id="1f638-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="1f638-131">NOTES</span></span>

## <span data-ttu-id="1f638-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1f638-132">RELATED LINKS</span></span>

[<span data-ttu-id="1f638-133">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1f638-133">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1f638-134">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1f638-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1f638-135">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1f638-135">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)



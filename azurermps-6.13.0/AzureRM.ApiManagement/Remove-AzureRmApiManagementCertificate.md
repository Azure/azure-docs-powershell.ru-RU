---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: a70e3323bbd154005f014f1064a535f45a102f8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556944"
---
# <span data-ttu-id="2fa3a-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2fa3a-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="2fa3a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2fa3a-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa3a-103">Удаляет сертификат управления API.</span><span class="sxs-lookup"><span data-stu-id="2fa3a-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fa3a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2fa3a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fa3a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fa3a-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa3a-106">Командлет **Remove-AzureRmApiManagementCertificate** Удаляет сертификат управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa3a-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="2fa3a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2fa3a-107">EXAMPLES</span></span>

### <span data-ttu-id="2fa3a-108">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="2fa3a-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="2fa3a-109">Эта команда удаляет указанный сертификат управления API.</span><span class="sxs-lookup"><span data-stu-id="2fa3a-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="2fa3a-110">Так как указан параметр *Force* , подтверждение не требуется.</span><span class="sxs-lookup"><span data-stu-id="2fa3a-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="2fa3a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2fa3a-111">PARAMETERS</span></span>

### <span data-ttu-id="2fa3a-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="2fa3a-112">-CertificateId</span></span>
<span data-ttu-id="2fa3a-113">Указывает ИД сертификата, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2fa3a-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="2fa3a-114">-Context</span><span class="sxs-lookup"><span data-stu-id="2fa3a-114">-Context</span></span>
<span data-ttu-id="2fa3a-115">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="2fa3a-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2fa3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa3a-116">-DefaultProfile</span></span>
<span data-ttu-id="2fa3a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2fa3a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fa3a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fa3a-118">-PassThru</span></span>
<span data-ttu-id="2fa3a-119">PassThru</span><span class="sxs-lookup"><span data-stu-id="2fa3a-119">passthru</span></span>

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

### <span data-ttu-id="2fa3a-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fa3a-120">-Confirm</span></span>
<span data-ttu-id="2fa3a-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2fa3a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fa3a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fa3a-122">-WhatIf</span></span>
<span data-ttu-id="2fa3a-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2fa3a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fa3a-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2fa3a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fa3a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa3a-125">CommonParameters</span></span>
<span data-ttu-id="2fa3a-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2fa3a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa3a-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa3a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa3a-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2fa3a-128">INPUTS</span></span>

### <span data-ttu-id="2fa3a-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2fa3a-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2fa3a-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2fa3a-130">System.String</span></span>

### <span data-ttu-id="2fa3a-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2fa3a-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2fa3a-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2fa3a-132">OUTPUTS</span></span>

### <span data-ttu-id="2fa3a-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2fa3a-133">System.Boolean</span></span>

## <span data-ttu-id="2fa3a-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="2fa3a-134">NOTES</span></span>

## <span data-ttu-id="2fa3a-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2fa3a-135">RELATED LINKS</span></span>

[<span data-ttu-id="2fa3a-136">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2fa3a-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="2fa3a-137">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2fa3a-137">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="2fa3a-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="2fa3a-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: 7e07d6a23f88f869c75c9d2bcbb8b0270f92ebb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901670"
---
# <span data-ttu-id="4dd08-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4dd08-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="4dd08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4dd08-102">SYNOPSIS</span></span>
<span data-ttu-id="4dd08-103">Удаляет сертификат управления API.</span><span class="sxs-lookup"><span data-stu-id="4dd08-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="4dd08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4dd08-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4dd08-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dd08-105">DESCRIPTION</span></span>
<span data-ttu-id="4dd08-106">Командлет **Remove-AzApiManagementCertificate** Удаляет сертификат управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd08-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="4dd08-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4dd08-107">EXAMPLES</span></span>

### <span data-ttu-id="4dd08-108">Пример 1: Удаление сертификата</span><span class="sxs-lookup"><span data-stu-id="4dd08-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="4dd08-109">Эта команда удаляет указанный сертификат управления API.</span><span class="sxs-lookup"><span data-stu-id="4dd08-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="4dd08-110">Так как указан параметр *Force* , подтверждение не требуется.</span><span class="sxs-lookup"><span data-stu-id="4dd08-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="4dd08-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4dd08-111">PARAMETERS</span></span>

### <span data-ttu-id="4dd08-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="4dd08-112">-CertificateId</span></span>
<span data-ttu-id="4dd08-113">Указывает ИД сертификата, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="4dd08-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="4dd08-114">-Context</span><span class="sxs-lookup"><span data-stu-id="4dd08-114">-Context</span></span>
<span data-ttu-id="4dd08-115">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4dd08-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4dd08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dd08-116">-DefaultProfile</span></span>
<span data-ttu-id="4dd08-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4dd08-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4dd08-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dd08-118">-PassThru</span></span>
<span data-ttu-id="4dd08-119">PassThru</span><span class="sxs-lookup"><span data-stu-id="4dd08-119">passthru</span></span>

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

### <span data-ttu-id="4dd08-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4dd08-120">-Confirm</span></span>
<span data-ttu-id="4dd08-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4dd08-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dd08-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dd08-122">-WhatIf</span></span>
<span data-ttu-id="4dd08-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4dd08-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dd08-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4dd08-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dd08-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dd08-125">CommonParameters</span></span>
<span data-ttu-id="4dd08-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4dd08-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dd08-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4dd08-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dd08-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4dd08-128">INPUTS</span></span>

### <span data-ttu-id="4dd08-129">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4dd08-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4dd08-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4dd08-130">System.String</span></span>

### <span data-ttu-id="4dd08-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4dd08-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4dd08-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4dd08-132">OUTPUTS</span></span>

### <span data-ttu-id="4dd08-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4dd08-133">System.Boolean</span></span>

## <span data-ttu-id="4dd08-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="4dd08-134">NOTES</span></span>

## <span data-ttu-id="4dd08-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4dd08-135">RELATED LINKS</span></span>

[<span data-ttu-id="4dd08-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4dd08-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="4dd08-137">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4dd08-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="4dd08-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4dd08-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)



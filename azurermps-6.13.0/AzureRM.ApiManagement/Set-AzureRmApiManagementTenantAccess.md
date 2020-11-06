---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementTenantAccess.md
ms.openlocfilehash: c8f05c7ca9ddeb5868d62633600d63f5d7f01be0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558599"
---
# <span data-ttu-id="db6fc-101">Set-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="db6fc-101">Set-AzureRmApiManagementTenantAccess</span></span>

## <span data-ttu-id="db6fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="db6fc-102">SYNOPSIS</span></span>
<span data-ttu-id="db6fc-103">Включает или выключает доступ клиентов.</span><span class="sxs-lookup"><span data-stu-id="db6fc-103">Enables or disables tenant access.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db6fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="db6fc-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db6fc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="db6fc-105">DESCRIPTION</span></span>
<span data-ttu-id="db6fc-106">Командлет **Set-AzureRmApiManagementTenantAccess** включает или выключает доступ клиентов.</span><span class="sxs-lookup"><span data-stu-id="db6fc-106">The **Set-AzureRmApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="db6fc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="db6fc-107">EXAMPLES</span></span>

### <span data-ttu-id="db6fc-108">Пример 1: разрешение доступа к клиенту</span><span class="sxs-lookup"><span data-stu-id="db6fc-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="db6fc-109">Эта команда включает клиентский доступ в указанном контексте.</span><span class="sxs-lookup"><span data-stu-id="db6fc-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="db6fc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="db6fc-110">PARAMETERS</span></span>

### <span data-ttu-id="db6fc-111">-Context</span><span class="sxs-lookup"><span data-stu-id="db6fc-111">-Context</span></span>
<span data-ttu-id="db6fc-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="db6fc-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="db6fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6fc-113">-DefaultProfile</span></span>
<span data-ttu-id="db6fc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="db6fc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db6fc-115">-Включено</span><span class="sxs-lookup"><span data-stu-id="db6fc-115">-Enabled</span></span>
<span data-ttu-id="db6fc-116">Указывает, будет ли этот командлет включать или отключать доступ клиента.</span><span class="sxs-lookup"><span data-stu-id="db6fc-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="db6fc-117">Укажите значение $True, чтобы включить или отключить или $False.</span><span class="sxs-lookup"><span data-stu-id="db6fc-117">Specify a value of $True to enable or $False to disable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db6fc-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db6fc-118">-PassThru</span></span>
<span data-ttu-id="db6fc-119">Указывает на то, что этот командлет возвращает **PsApiManagementAccessInformation** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="db6fc-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="db6fc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6fc-120">CommonParameters</span></span>
<span data-ttu-id="db6fc-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="db6fc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6fc-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6fc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6fc-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="db6fc-123">INPUTS</span></span>

### <span data-ttu-id="db6fc-124">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="db6fc-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="db6fc-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="db6fc-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="db6fc-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="db6fc-126">OUTPUTS</span></span>

### <span data-ttu-id="db6fc-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="db6fc-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="db6fc-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="db6fc-128">NOTES</span></span>

## <span data-ttu-id="db6fc-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="db6fc-129">RELATED LINKS</span></span>

[<span data-ttu-id="db6fc-130">Get-AzureRmApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="db6fc-130">Get-AzureRmApiManagementTenantAccess</span></span>](./Get-AzureRmApiManagementTenantAccess.md)



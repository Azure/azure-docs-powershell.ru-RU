---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 5f14a0698c0b1ea950a28236a8a523734b2ddf5e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901557"
---
# <span data-ttu-id="4577b-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="4577b-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="4577b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4577b-102">SYNOPSIS</span></span>
<span data-ttu-id="4577b-103">Включает или выключает доступ клиентов.</span><span class="sxs-lookup"><span data-stu-id="4577b-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="4577b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4577b-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4577b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4577b-105">DESCRIPTION</span></span>
<span data-ttu-id="4577b-106">Командлет **Set-AzApiManagementTenantAccess** включает или выключает доступ клиентов.</span><span class="sxs-lookup"><span data-stu-id="4577b-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="4577b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4577b-107">EXAMPLES</span></span>

### <span data-ttu-id="4577b-108">Пример 1: разрешение доступа к клиенту</span><span class="sxs-lookup"><span data-stu-id="4577b-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="4577b-109">Эта команда включает клиентский доступ в указанном контексте.</span><span class="sxs-lookup"><span data-stu-id="4577b-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="4577b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4577b-110">PARAMETERS</span></span>

### <span data-ttu-id="4577b-111">-Context</span><span class="sxs-lookup"><span data-stu-id="4577b-111">-Context</span></span>
<span data-ttu-id="4577b-112">Указывает объект **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4577b-112">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4577b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4577b-113">-DefaultProfile</span></span>
<span data-ttu-id="4577b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4577b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4577b-115">-Включено</span><span class="sxs-lookup"><span data-stu-id="4577b-115">-Enabled</span></span>
<span data-ttu-id="4577b-116">Указывает, будет ли этот командлет включать или отключать доступ клиента.</span><span class="sxs-lookup"><span data-stu-id="4577b-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="4577b-117">Укажите значение $True, чтобы включить или отключить или $False.</span><span class="sxs-lookup"><span data-stu-id="4577b-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="4577b-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4577b-118">-PassThru</span></span>
<span data-ttu-id="4577b-119">Указывает на то, что этот командлет возвращает **PsApiManagementAccessInformation** , который изменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4577b-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="4577b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4577b-120">CommonParameters</span></span>
<span data-ttu-id="4577b-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4577b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4577b-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4577b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4577b-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4577b-123">INPUTS</span></span>

### <span data-ttu-id="4577b-124">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4577b-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4577b-125">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4577b-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4577b-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4577b-126">OUTPUTS</span></span>

### <span data-ttu-id="4577b-127">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="4577b-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="4577b-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="4577b-128">NOTES</span></span>

## <span data-ttu-id="4577b-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4577b-129">RELATED LINKS</span></span>

[<span data-ttu-id="4577b-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="4577b-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)



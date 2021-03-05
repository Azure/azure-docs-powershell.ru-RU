---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 3B5FC8E3-5A02-4F3B-81F0-51DFE47A201B
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementtenantaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementTenantAccess.md
ms.openlocfilehash: 1685b9607108fa0b7795fb0ed2c69eb94735fc5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978963"
---
# <span data-ttu-id="97a13-101">Set-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="97a13-101">Set-AzApiManagementTenantAccess</span></span>

## <span data-ttu-id="97a13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97a13-102">SYNOPSIS</span></span>
<span data-ttu-id="97a13-103">Включает или отключает клиентский доступ.</span><span class="sxs-lookup"><span data-stu-id="97a13-103">Enables or disables tenant access.</span></span>

## <span data-ttu-id="97a13-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="97a13-104">SYNTAX</span></span>

```
Set-AzApiManagementTenantAccess -Context <PsApiManagementContext> -Enabled <Boolean> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97a13-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97a13-105">DESCRIPTION</span></span>
<span data-ttu-id="97a13-106">С **помощью cmdlet Set-AzApiManagementTenantAccess** можно включить или отключить клиентский доступ.</span><span class="sxs-lookup"><span data-stu-id="97a13-106">The **Set-AzApiManagementTenantAccess** cmdlet enables or disables tenant access.</span></span>

## <span data-ttu-id="97a13-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="97a13-107">EXAMPLES</span></span>

### <span data-ttu-id="97a13-108">Пример 1. Включить клиентский доступ</span><span class="sxs-lookup"><span data-stu-id="97a13-108">Example 1: Enable tenant access</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementTenantAccess -Context $apimContext -Enabled $True
```

<span data-ttu-id="97a13-109">Эта команда обеспечивает доступ клиента в указанном контексте.</span><span class="sxs-lookup"><span data-stu-id="97a13-109">This command enables tenant access in the specified context.</span></span>

## <span data-ttu-id="97a13-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97a13-110">PARAMETERS</span></span>

### <span data-ttu-id="97a13-111">-Контекст</span><span class="sxs-lookup"><span data-stu-id="97a13-111">-Context</span></span>
<span data-ttu-id="97a13-112">Указывает объект **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="97a13-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97a13-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a13-113">-DefaultProfile</span></span>
<span data-ttu-id="97a13-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="97a13-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="97a13-115">-Enabled</span><span class="sxs-lookup"><span data-stu-id="97a13-115">-Enabled</span></span>
<span data-ttu-id="97a13-116">Указывает, включает ли этот cmdlet доступ к клиенту.</span><span class="sxs-lookup"><span data-stu-id="97a13-116">Specifies whether this cmdlet enables or disables tenant access.</span></span>
<span data-ttu-id="97a13-117">Укажите значение, которое $True включить или $False отключить.</span><span class="sxs-lookup"><span data-stu-id="97a13-117">Specify a value of $True to enable or $False to disable.</span></span>

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

### <span data-ttu-id="97a13-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97a13-118">-PassThru</span></span>
<span data-ttu-id="97a13-119">Указывает на то, что этот cmdlet возвращает **psApiManagementAccessInformation,** который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97a13-119">Indicates that this cmdlet returns the **PsApiManagementAccessInformation** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="97a13-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a13-120">CommonParameters</span></span>
<span data-ttu-id="97a13-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97a13-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a13-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97a13-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a13-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="97a13-123">INPUTS</span></span>

### <span data-ttu-id="97a13-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="97a13-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="97a13-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="97a13-125">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="97a13-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="97a13-126">OUTPUTS</span></span>

### <span data-ttu-id="97a13-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span><span class="sxs-lookup"><span data-stu-id="97a13-127">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementAccessInformation</span></span>

## <span data-ttu-id="97a13-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="97a13-128">NOTES</span></span>

## <span data-ttu-id="97a13-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97a13-129">RELATED LINKS</span></span>

[<span data-ttu-id="97a13-130">Get-AzApiManagementTenantAccess</span><span class="sxs-lookup"><span data-stu-id="97a13-130">Get-AzApiManagementTenantAccess</span></span>](./Get-AzApiManagementTenantAccess.md)



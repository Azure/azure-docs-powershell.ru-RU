---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 8b8ac352819b9b3ec7cd655501c5bf8cfbba6816
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728095"
---
# <span data-ttu-id="05c08-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="05c08-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="05c08-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="05c08-102">SYNOPSIS</span></span>
<span data-ttu-id="05c08-103">Возвращает ссылку с маркером единого входа на развернутый портал управления в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="05c08-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="05c08-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="05c08-104">SYNTAX</span></span>

### <span data-ttu-id="05c08-105">ExpandedParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="05c08-105">ExpandedParameter (Default)</span></span>
```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05c08-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="05c08-106">ByInputObject</span></span>
```
Get-AzApiManagementSsoToken -InputObject <PsApiManagement> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05c08-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="05c08-107">DESCRIPTION</span></span>
<span data-ttu-id="05c08-108">Командлет **Get-AzApiManagementSsoToken** возвращает ссылку (URL-адрес), содержащую маркер единого входа (SSO), на развернутый портал управления для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="05c08-108">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="05c08-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="05c08-109">EXAMPLES</span></span>

### <span data-ttu-id="05c08-110">Пример 1: получение маркера единого входа для службы управления API</span><span class="sxs-lookup"><span data-stu-id="05c08-110">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="05c08-111">Эта команда получает маркер SSO службы управления API.</span><span class="sxs-lookup"><span data-stu-id="05c08-111">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="05c08-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="05c08-112">PARAMETERS</span></span>

### <span data-ttu-id="05c08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c08-113">-DefaultProfile</span></span>
<span data-ttu-id="05c08-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="05c08-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05c08-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05c08-115">-InputObject</span></span>
<span data-ttu-id="05c08-116">Экземпляр PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="05c08-116">Instance of PsApiManagement.</span></span> <span data-ttu-id="05c08-117">Этот параметр является обязательным.</span><span class="sxs-lookup"><span data-stu-id="05c08-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05c08-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="05c08-118">-Name</span></span>
<span data-ttu-id="05c08-119">Указывает имя экземпляра управления API.</span><span class="sxs-lookup"><span data-stu-id="05c08-119">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05c08-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05c08-120">-ResourceGroupName</span></span>
<span data-ttu-id="05c08-121">Указывает имя группы ресурсов, для которой существует управление API.</span><span class="sxs-lookup"><span data-stu-id="05c08-121">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05c08-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c08-122">CommonParameters</span></span>
<span data-ttu-id="05c08-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="05c08-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c08-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05c08-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c08-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="05c08-125">INPUTS</span></span>

### <span data-ttu-id="05c08-126">System. String</span><span class="sxs-lookup"><span data-stu-id="05c08-126">System.String</span></span>

## <span data-ttu-id="05c08-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="05c08-127">OUTPUTS</span></span>

### <span data-ttu-id="05c08-128">System. String</span><span class="sxs-lookup"><span data-stu-id="05c08-128">System.String</span></span>

## <span data-ttu-id="05c08-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="05c08-129">NOTES</span></span>

## <span data-ttu-id="05c08-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="05c08-130">RELATED LINKS</span></span>

[<span data-ttu-id="05c08-131">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="05c08-131">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)



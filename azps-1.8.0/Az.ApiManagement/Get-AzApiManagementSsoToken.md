---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A7CABC63-2E9C-474B-A4F0-69F13A16F65A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementssotoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSsoToken.md
ms.openlocfilehash: 40c9166ab650f7cb31ac53c55397bb7bc635f6e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720136"
---
# <span data-ttu-id="6021f-101">Get-AzApiManagementSsoToken</span><span class="sxs-lookup"><span data-stu-id="6021f-101">Get-AzApiManagementSsoToken</span></span>

## <span data-ttu-id="6021f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6021f-102">SYNOPSIS</span></span>
<span data-ttu-id="6021f-103">Возвращает ссылку с маркером единого входа на развернутый портал управления в службе управления API.</span><span class="sxs-lookup"><span data-stu-id="6021f-103">Gets a link with an SSO token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="6021f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6021f-104">SYNTAX</span></span>

```
Get-AzApiManagementSsoToken -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6021f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6021f-105">DESCRIPTION</span></span>
<span data-ttu-id="6021f-106">Командлет **Get-AzApiManagementSsoToken** возвращает ссылку (URL-адрес), содержащую маркер единого входа (SSO), на развернутый портал управления для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="6021f-106">The **Get-AzApiManagementSsoToken** cmdlet returns a link (URL) containing a single sign-on (SSO) token to a deployed management portal of an API Management service.</span></span>

## <span data-ttu-id="6021f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6021f-107">EXAMPLES</span></span>

### <span data-ttu-id="6021f-108">Пример 1: получение маркера единого входа для службы управления API</span><span class="sxs-lookup"><span data-stu-id="6021f-108">Example 1: Get the SSO token of an API Management service</span></span>
```
PS C:\>Get-AzApiManagementSsoToken -ResourceGroupName "Contoso" -Name "ContosoApi"
```

<span data-ttu-id="6021f-109">Эта команда получает маркер SSO службы управления API.</span><span class="sxs-lookup"><span data-stu-id="6021f-109">This command gets the SSO token of an API Management service.</span></span>

## <span data-ttu-id="6021f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6021f-110">PARAMETERS</span></span>

### <span data-ttu-id="6021f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6021f-111">-DefaultProfile</span></span>
<span data-ttu-id="6021f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6021f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6021f-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6021f-113">-Name</span></span>
<span data-ttu-id="6021f-114">Указывает имя экземпляра управления API.</span><span class="sxs-lookup"><span data-stu-id="6021f-114">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="6021f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6021f-115">-ResourceGroupName</span></span>
<span data-ttu-id="6021f-116">Указывает имя группы ресурсов, для которой существует управление API.</span><span class="sxs-lookup"><span data-stu-id="6021f-116">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="6021f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6021f-117">CommonParameters</span></span>
<span data-ttu-id="6021f-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6021f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6021f-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6021f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6021f-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6021f-120">INPUTS</span></span>

### <span data-ttu-id="6021f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6021f-121">System.String</span></span>

## <span data-ttu-id="6021f-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6021f-122">OUTPUTS</span></span>

### <span data-ttu-id="6021f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="6021f-123">System.String</span></span>

## <span data-ttu-id="6021f-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="6021f-124">NOTES</span></span>

## <span data-ttu-id="6021f-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6021f-125">RELATED LINKS</span></span>

[<span data-ttu-id="6021f-126">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="6021f-126">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)



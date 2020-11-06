---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: D4C465CE-1B8A-4CFC-BAA8-21CC66B7D6D6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementHostnameConfiguration.md
ms.openlocfilehash: 1b34903f402f7e8d432d16087f1e32fc7b7da3e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565729"
---
# <span data-ttu-id="f3d26-101">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3d26-101">New-AzureRmApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="f3d26-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3d26-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d26-103">Создает экземпляр PsApiManagementHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="f3d26-103">Creates an instance of PsApiManagementHostnameConfiguration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3d26-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3d26-104">SYNTAX</span></span>

```
New-AzureRmApiManagementHostnameConfiguration -CertificateThumbprint <String> -Hostname <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3d26-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3d26-105">DESCRIPTION</span></span>
<span data-ttu-id="f3d26-106">Командлет **New-AzureRmApiManagementHostnameConfiguration** является вспомогательной командой, которая создает экземпляр **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f3d26-106">The **New-AzureRmApiManagementHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementHostnameConfiguration**.</span></span>
<span data-ttu-id="f3d26-107">Эта команда используется с командлетом Set-AzureRmApiManagementHostnames.</span><span class="sxs-lookup"><span data-stu-id="f3d26-107">This command is used with the Set-AzureRmApiManagementHostnames cmdlet.</span></span>

## <span data-ttu-id="f3d26-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3d26-108">EXAMPLES</span></span>

### <span data-ttu-id="f3d26-109">Пример 1: создание и инициализация экземпляра PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3d26-109">Example 1: Create and initialize an instance of PsApiManagementHostnameConfiguration</span></span>
```
PS C:\>New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
```

<span data-ttu-id="f3d26-110">Эта команда создает и инициализирует экземпляр **PsApiManagementHostnameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f3d26-110">This command creates and initializes an instance of **PsApiManagementHostnameConfiguration**.</span></span>

## <span data-ttu-id="f3d26-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3d26-111">PARAMETERS</span></span>

### <span data-ttu-id="f3d26-112">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="f3d26-112">-CertificateThumbprint</span></span>
<span data-ttu-id="f3d26-113">Указывает отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="f3d26-113">Specifies the certificate thumbprint.</span></span>
<span data-ttu-id="f3d26-114">Сертификат необходимо сначала импортировать с помощью командлета Import-AzureRmApiManagementHostnameCertificate.</span><span class="sxs-lookup"><span data-stu-id="f3d26-114">The certificate must be first imported with the Import-AzureRmApiManagementHostnameCertificate cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d26-115">-Hostname</span><span class="sxs-lookup"><span data-stu-id="f3d26-115">-Hostname</span></span>
<span data-ttu-id="f3d26-116">Задает настраиваемое имя узла, для которого этот командлет создает экземпляр **PsApiManagementHostnameConfiguration** .</span><span class="sxs-lookup"><span data-stu-id="f3d26-116">Specifies the custom host name for which this cmdlet creates the **PsApiManagementHostnameConfiguration** instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d26-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d26-117">-DefaultProfile</span></span>
<span data-ttu-id="f3d26-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3d26-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3d26-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d26-119">CommonParameters</span></span>
<span data-ttu-id="f3d26-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3d26-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d26-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d26-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d26-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3d26-122">INPUTS</span></span>

## <span data-ttu-id="f3d26-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3d26-123">OUTPUTS</span></span>

### <span data-ttu-id="f3d26-124">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f3d26-124">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="f3d26-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3d26-125">NOTES</span></span>

## <span data-ttu-id="f3d26-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3d26-126">RELATED LINKS</span></span>

[<span data-ttu-id="f3d26-127">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f3d26-127">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="f3d26-128">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f3d26-128">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)



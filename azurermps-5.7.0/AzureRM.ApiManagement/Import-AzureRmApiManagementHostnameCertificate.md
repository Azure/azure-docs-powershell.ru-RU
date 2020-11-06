---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 98367100-4FFD-46F6-8974-603B32533626
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementhostnamecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
ms.openlocfilehash: 9c5f819a34ea0e394888e8156dad7a897d18167f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568656"
---
# <span data-ttu-id="10420-101">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="10420-101">Import-AzureRmApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="10420-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10420-102">SYNOPSIS</span></span>
<span data-ttu-id="10420-103">Импорт сертификата в формате PFX для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="10420-103">Imports a certificate in a PFX format for an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10420-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10420-104">SYNTAX</span></span>

```
Import-AzureRmApiManagementHostnameCertificate -ResourceGroupName <String> -Name <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> -PfxPassword <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10420-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10420-105">DESCRIPTION</span></span>
<span data-ttu-id="10420-106">Командлет **Import-AzureRmApiManagementHostnameCertificate** импортирует сертификат в формате PFX для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="10420-106">The **Import-AzureRmApiManagementHostnameCertificate** cmdlet imports a certificate in a PFX format for an API Management Service.</span></span>
<span data-ttu-id="10420-107">Этот сертификат используется для настраиваемых конфигураций hostname.</span><span class="sxs-lookup"><span data-stu-id="10420-107">The certificate is to be used for custom hostnames configuration.</span></span>

## <span data-ttu-id="10420-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10420-108">EXAMPLES</span></span>

### <span data-ttu-id="10420-109">Пример 1: Импорт сертификата узла управления API</span><span class="sxs-lookup"><span data-stu-id="10420-109">Example 1: Import a API Management hostname certificate</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName Contoso -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
```

<span data-ttu-id="10420-110">Эта команда импортирует сертификат для настраиваемого hostname прокси-сервера.</span><span class="sxs-lookup"><span data-stu-id="10420-110">This command imports a certificate for a proxy custom hostname.</span></span>

## <span data-ttu-id="10420-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10420-111">PARAMETERS</span></span>

### <span data-ttu-id="10420-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10420-112">-DefaultProfile</span></span>
<span data-ttu-id="10420-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10420-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="10420-114">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="10420-114">-HostnameType</span></span>
<span data-ttu-id="10420-115">Указывает тип имени узла, для которого этот командлет загружает сертификат.</span><span class="sxs-lookup"><span data-stu-id="10420-115">Specifies the host name type that this cmdlet loads the certificate for.</span></span>

<span data-ttu-id="10420-116">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="10420-116">Valid values are:</span></span> 

- <span data-ttu-id="10420-117">Посредник</span><span class="sxs-lookup"><span data-stu-id="10420-117">Proxy</span></span>
- <span data-ttu-id="10420-118">Узла</span><span class="sxs-lookup"><span data-stu-id="10420-118">Portal</span></span>

```yaml
Type: PsApiManagementHostnameType
Parameter Sets: (All)
Aliases: 
Accepted values: Proxy, Portal

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10420-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="10420-119">-Name</span></span>
<span data-ttu-id="10420-120">Указывает имя развертывания управления API, которое этот командлет импортирует.</span><span class="sxs-lookup"><span data-stu-id="10420-120">Specifies the name of the API Management deployment that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10420-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10420-121">-PassThru</span></span>
<span data-ttu-id="10420-122">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="10420-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="10420-123">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="10420-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10420-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="10420-124">-PfxPassword</span></span>
<span data-ttu-id="10420-125">Указывает пароль для PFX-файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="10420-125">Specifies the password for the .pfx certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10420-126">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="10420-126">-PfxPath</span></span>
<span data-ttu-id="10420-127">Указывает путь к PFX-файлу сертификата.</span><span class="sxs-lookup"><span data-stu-id="10420-127">Specifies the path to a .pfx certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10420-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10420-128">-ResourceGroupName</span></span>
<span data-ttu-id="10420-129">Указывает имя группы ресурсов, в которой находится развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="10420-129">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10420-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10420-130">CommonParameters</span></span>
<span data-ttu-id="10420-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10420-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10420-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10420-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10420-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10420-133">INPUTS</span></span>

### <span data-ttu-id="10420-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="10420-134">None</span></span>
<span data-ttu-id="10420-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="10420-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="10420-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10420-136">OUTPUTS</span></span>

### <span data-ttu-id="10420-137">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="10420-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="10420-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="10420-138">NOTES</span></span>

## <span data-ttu-id="10420-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10420-139">RELATED LINKS</span></span>

[<span data-ttu-id="10420-140">New-AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="10420-140">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

[<span data-ttu-id="10420-141">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="10420-141">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)



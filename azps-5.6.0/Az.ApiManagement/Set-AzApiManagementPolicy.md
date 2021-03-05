---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6CD1C2B8-0416-4FF3-81B0-0C9E59AE6CF9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementPolicy.md
ms.openlocfilehash: 3858d24bb0c714da0e48ad5834870ec5127eb5e5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965347"
---
# <span data-ttu-id="60940-101">Set-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="60940-101">Set-AzApiManagementPolicy</span></span>

## <span data-ttu-id="60940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60940-102">SYNOPSIS</span></span>
<span data-ttu-id="60940-103">Задает указанную политику области для управления API.</span><span class="sxs-lookup"><span data-stu-id="60940-103">Sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="60940-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="60940-104">SYNTAX</span></span>

### <span data-ttu-id="60940-105">SetTenantLevel (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="60940-105">SetTenantLevel (Default)</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-Policy <String>]
 [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60940-106">SetProductLevel</span><span class="sxs-lookup"><span data-stu-id="60940-106">SetProductLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ProductId <String>
 [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60940-107">SetApiLevel</span><span class="sxs-lookup"><span data-stu-id="60940-107">SetApiLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] [-Policy <String>] [-PolicyFilePath <String>] [-PolicyUrl <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60940-108">SetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="60940-108">SetOperationLevel</span></span>
```
Set-AzApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] -ApiId <String>
 [-ApiRevision <String>] -OperationId <String> [-Policy <String>] [-PolicyFilePath <String>]
 [-PolicyUrl <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60940-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="60940-109">DESCRIPTION</span></span>
<span data-ttu-id="60940-110">Для управления API задана политика области **Set-AzApiManagementPolicy.**</span><span class="sxs-lookup"><span data-stu-id="60940-110">The **Set-AzApiManagementPolicy** cmdlet sets the specified scope policy for API Management.</span></span>

## <span data-ttu-id="60940-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="60940-111">EXAMPLES</span></span>

### <span data-ttu-id="60940-112">Пример 1. Настройка политики на уровне клиента</span><span class="sxs-lookup"><span data-stu-id="60940-112">Example 1: Set the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -PolicyFilePath "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="60940-113">Эта команда задает политику на уровне клиента из файла с именем tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="60940-113">This command sets the tenant level policy from a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="60940-114">Пример 2. Настройка политики области продуктов</span><span class="sxs-lookup"><span data-stu-id="60940-114">Example 2: Set a product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ProductId "0123456789" -Policy $PolicyString
```

<span data-ttu-id="60940-115">Эта команда задает политику области продуктов для управления API.</span><span class="sxs-lookup"><span data-stu-id="60940-115">This command sets the product-scope policy for API Management.</span></span>

### <span data-ttu-id="60940-116">Пример 3. Настройка политики области API</span><span class="sxs-lookup"><span data-stu-id="60940-116">Example 3: Set API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -Policy $PolicyString
```

<span data-ttu-id="60940-117">Эта команда задает политику области API для управления API.</span><span class="sxs-lookup"><span data-stu-id="60940-117">This command sets API-scope policy for API Management.</span></span>

### <span data-ttu-id="60940-118">Пример 4. Настройка политики области действия</span><span class="sxs-lookup"><span data-stu-id="60940-118">Example 4: Set operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777" -Policy $PolicyString
```

<span data-ttu-id="60940-119">Эта команда задает политику области действия для управления API.</span><span class="sxs-lookup"><span data-stu-id="60940-119">This command sets operation-scope policy for API Management.</span></span>

## <span data-ttu-id="60940-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60940-120">PARAMETERS</span></span>

### <span data-ttu-id="60940-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="60940-121">-ApiId</span></span>
<span data-ttu-id="60940-122">Указывает идентификатор существующего API.</span><span class="sxs-lookup"><span data-stu-id="60940-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="60940-123">Если этот параметр задан, будет задана политика области API.</span><span class="sxs-lookup"><span data-stu-id="60940-123">If you specify this parameter, the cmdlet sets the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60940-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="60940-124">-ApiRevision</span></span>
<span data-ttu-id="60940-125">Идентификатор изменения API.</span><span class="sxs-lookup"><span data-stu-id="60940-125">Identifier of API Revision.</span></span> <span data-ttu-id="60940-126">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="60940-126">This parameter is optional.</span></span> <span data-ttu-id="60940-127">Если не указано, политика будет обновлена в активной редакции API.</span><span class="sxs-lookup"><span data-stu-id="60940-127">If not specified, the policy will be updated in the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: SetApiLevel, SetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60940-128">-Контекст</span><span class="sxs-lookup"><span data-stu-id="60940-128">-Context</span></span>
<span data-ttu-id="60940-129">Указывает экземпляр **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="60940-129">Specifies the instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="60940-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60940-130">-DefaultProfile</span></span>
<span data-ttu-id="60940-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="60940-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60940-132">-Format</span><span class="sxs-lookup"><span data-stu-id="60940-132">-Format</span></span>
<span data-ttu-id="60940-133">Формат политики.</span><span class="sxs-lookup"><span data-stu-id="60940-133">Specifies the format of the policy.</span></span> <span data-ttu-id="60940-134">При использовании `application/vnd.ms-azure-apim.policy+xml` выражений, содержащихся в политике, должен быть XML-escaped.</span><span class="sxs-lookup"><span data-stu-id="60940-134">When using `application/vnd.ms-azure-apim.policy+xml`, expressions contained within the policy must be XML-escaped.</span></span> <span data-ttu-id="60940-135">Для `application/vnd.ms-azure-apim.policy.raw+xml` использования политики **не** требуется использовать escape-escape-XML.</span><span class="sxs-lookup"><span data-stu-id="60940-135">When using `application/vnd.ms-azure-apim.policy.raw+xml` it is **not** necessary for the policy to be XML-escaped.</span></span>
<span data-ttu-id="60940-136">Значение по `application/vnd.ms-azure-apim.policy+xml` умолчанию: .</span><span class="sxs-lookup"><span data-stu-id="60940-136">The default value is `application/vnd.ms-azure-apim.policy+xml`.</span></span>
<span data-ttu-id="60940-137">Этот параметр является необязательным.</span><span class="sxs-lookup"><span data-stu-id="60940-137">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60940-138">-OperationId</span><span class="sxs-lookup"><span data-stu-id="60940-138">-OperationId</span></span>
<span data-ttu-id="60940-139">Указывает идентификатор существующей операции.</span><span class="sxs-lookup"><span data-stu-id="60940-139">Specifies the identifier of the existing operation.</span></span>
<span data-ttu-id="60940-140">Если задана политика ApiId, задана политика области действия.</span><span class="sxs-lookup"><span data-stu-id="60940-140">If specified with ApiId will set operation-scope policy.</span></span>
<span data-ttu-id="60940-141">Эти параметры необходимы.</span><span class="sxs-lookup"><span data-stu-id="60940-141">This parameters is required.</span></span>

```yaml
Type: System.String
Parameter Sets: SetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60940-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60940-142">-PassThru</span></span>
<span data-ttu-id="60940-143">passthru</span><span class="sxs-lookup"><span data-stu-id="60940-143">passthru</span></span>

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

### <span data-ttu-id="60940-144">-Политика</span><span class="sxs-lookup"><span data-stu-id="60940-144">-Policy</span></span>
<span data-ttu-id="60940-145">Определяет документ политики в качестве строки.</span><span class="sxs-lookup"><span data-stu-id="60940-145">Specifies the policy document as a string.</span></span>
<span data-ttu-id="60940-146">Этот параметр является required, если параметр *- PolicyFilePath* не указан.</span><span class="sxs-lookup"><span data-stu-id="60940-146">This parameter is required if the -*PolicyFilePath* is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60940-147">-PolicyFilePath</span><span class="sxs-lookup"><span data-stu-id="60940-147">-PolicyFilePath</span></span>
<span data-ttu-id="60940-148">Путь к файлу документа политики.</span><span class="sxs-lookup"><span data-stu-id="60940-148">Specifies the policy document file path.</span></span>
<span data-ttu-id="60940-149">Этот параметр является required, если параметр *policy* не указан.</span><span class="sxs-lookup"><span data-stu-id="60940-149">This parameter is required if the *Policy* parameter is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60940-150">-PolicyUrl</span><span class="sxs-lookup"><span data-stu-id="60940-150">-PolicyUrl</span></span>
<span data-ttu-id="60940-151">URL-адрес, на котором размещен документ политики.</span><span class="sxs-lookup"><span data-stu-id="60940-151">The Url where the Policy document is hosted.</span></span> <span data-ttu-id="60940-152">Этот параметр является required, если параметр -Policy или -PolicyFilePath не указан.</span><span class="sxs-lookup"><span data-stu-id="60940-152">This parameter is required if -Policy or -PolicyFilePath is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60940-153">-ProductId</span><span class="sxs-lookup"><span data-stu-id="60940-153">-ProductId</span></span>
<span data-ttu-id="60940-154">Определяет идентификатор существующего продукта.</span><span class="sxs-lookup"><span data-stu-id="60940-154">Specifies the identifier of the existing product.</span></span>
<span data-ttu-id="60940-155">Если этот параметр задан, будет задана политика области действия продукта.</span><span class="sxs-lookup"><span data-stu-id="60940-155">If this parameter is specified, the cmdlet sets the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60940-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60940-156">CommonParameters</span></span>
<span data-ttu-id="60940-157">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60940-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60940-158">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60940-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60940-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60940-159">INPUTS</span></span>

### <span data-ttu-id="60940-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="60940-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="60940-161">System.String</span><span class="sxs-lookup"><span data-stu-id="60940-161">System.String</span></span>

### <span data-ttu-id="60940-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="60940-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="60940-163">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="60940-163">OUTPUTS</span></span>

### <span data-ttu-id="60940-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="60940-164">System.Boolean</span></span>

## <span data-ttu-id="60940-165">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="60940-165">NOTES</span></span>

## <span data-ttu-id="60940-166">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="60940-166">RELATED LINKS</span></span>

[<span data-ttu-id="60940-167">Get-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="60940-167">Get-AzApiManagementPolicy</span></span>](./Get-AzApiManagementPolicy.md)

[<span data-ttu-id="60940-168">Remove-AzApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="60940-168">Remove-AzApiManagementPolicy</span></span>](./Remove-AzApiManagementPolicy.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B30C2BDD-6DA9-47B5-88FE-3AD43E15A072
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverkeyvaultcredentialconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerKeyVaultCredentialConfig.md
ms.openlocfilehash: 50bf29524e4c16a7a7186a547505f4dcf7dac4e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504653"
---
# <span data-ttu-id="0337d-101">New-AzVMSqlServerKeyVaultCredentialConfig</span><span class="sxs-lookup"><span data-stu-id="0337d-101">New-AzVMSqlServerKeyVaultCredentialConfig</span></span>

## <span data-ttu-id="0337d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0337d-102">SYNOPSIS</span></span>
<span data-ttu-id="0337d-103">Создает объект конфигурации для SQL ключа сервера на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0337d-103">Creates a configuration object for SQL server key vault credential on a virtual machine.</span></span>

## <span data-ttu-id="0337d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0337d-104">SYNTAX</span></span>

```
New-AzVMSqlServerKeyVaultCredentialConfig [-ResourceGroupName] <String> [-Enable] [-CredentialName <String>]
 [-AzureKeyVaultUrl <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <SecureString>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0337d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0337d-105">DESCRIPTION</span></span>

## <span data-ttu-id="0337d-106">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0337d-106">EXAMPLES</span></span>

## <span data-ttu-id="0337d-107">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0337d-107">PARAMETERS</span></span>

### <span data-ttu-id="0337d-108">-AzureKeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="0337d-108">-AzureKeyVaultUrl</span></span>
<span data-ttu-id="0337d-109">URL-адрес службы хранилища ключей Azure</span><span class="sxs-lookup"><span data-stu-id="0337d-109">Azure Key Vault service URL</span></span>

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

### <span data-ttu-id="0337d-110">-CredentialName</span><span class="sxs-lookup"><span data-stu-id="0337d-110">-CredentialName</span></span>
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

### <span data-ttu-id="0337d-111">-Enable</span><span class="sxs-lookup"><span data-stu-id="0337d-111">-Enable</span></span>
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

### <span data-ttu-id="0337d-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0337d-112">-ResourceGroupName</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0337d-113">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0337d-113">-ServicePrincipalName</span></span>
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

### <span data-ttu-id="0337d-114">-ServicePrincipalSecret</span><span class="sxs-lookup"><span data-stu-id="0337d-114">-ServicePrincipalSecret</span></span>
```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0337d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0337d-115">-Confirm</span></span>
<span data-ttu-id="0337d-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0337d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0337d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0337d-117">-WhatIf</span></span>
<span data-ttu-id="0337d-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0337d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0337d-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0337d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0337d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0337d-120">CommonParameters</span></span>
<span data-ttu-id="0337d-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0337d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0337d-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0337d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0337d-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0337d-123">INPUTS</span></span>

### <span data-ttu-id="0337d-124">System.String</span><span class="sxs-lookup"><span data-stu-id="0337d-124">System.String</span></span>

### <span data-ttu-id="0337d-125">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0337d-125">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0337d-126">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="0337d-126">System.Security.SecureString</span></span>

## <span data-ttu-id="0337d-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0337d-127">OUTPUTS</span></span>

### <span data-ttu-id="0337d-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="0337d-128">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="0337d-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0337d-129">NOTES</span></span>

## <span data-ttu-id="0337d-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0337d-130">RELATED LINKS</span></span>

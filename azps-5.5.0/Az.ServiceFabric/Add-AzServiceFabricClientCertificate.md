---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/add-azservicefabricclientcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Add-AzServiceFabricClientCertificate.md
ms.openlocfilehash: ca9dbbba29e6f770b727e1f96717c2626f112839
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232732"
---
# <span data-ttu-id="89fc1-101">Add-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="89fc1-101">Add-AzServiceFabricClientCertificate</span></span>

## <span data-ttu-id="89fc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89fc1-102">SYNOPSIS</span></span>
<span data-ttu-id="89fc1-103">Добавьте общие имена или эскизы в кластер в целях проверки подлинности клиента.</span><span class="sxs-lookup"><span data-stu-id="89fc1-103">Add common name or thumbprint to the cluster for client authentication purposes.</span></span>

## <span data-ttu-id="89fc1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89fc1-104">SYNTAX</span></span>

### <span data-ttu-id="89fc1-105">SingleUpdateWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="89fc1-105">SingleUpdateWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -Thumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89fc1-106">SingleUpdateWithCommonName</span><span class="sxs-lookup"><span data-stu-id="89fc1-106">SingleUpdateWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-Admin] [-ResourceGroupName] <String> [-Name] <String>
 -CommonName <String> -IssuerThumbprint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89fc1-107">MultipleUpdatesWithCommonName</span><span class="sxs-lookup"><span data-stu-id="89fc1-107">MultipleUpdatesWithCommonName</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 -ClientCertificateCommonName <PSClientCertificateCommonName[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89fc1-108">MultipleUpdatesWithThumbprint</span><span class="sxs-lookup"><span data-stu-id="89fc1-108">MultipleUpdatesWithThumbprint</span></span>
```
Add-AzServiceFabricClientCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-AdminClientThumbprint <String[]>] [-ReadonlyClientThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="89fc1-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89fc1-109">DESCRIPTION</span></span>
<span data-ttu-id="89fc1-110">Добавьте общие имена и эскизы сертификатов выдачи в кластер с помощью **Add-AzServiceFabricClientCertificate,** чтобы клиент сможет использовать их для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="89fc1-110">Use **Add-AzServiceFabricClientCertificate** to add a common name and issuer thumbprint or certificate thumbprint to the cluster, so the client can use it for authentication.</span></span>

## <span data-ttu-id="89fc1-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89fc1-111">EXAMPLES</span></span>

### <span data-ttu-id="89fc1-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="89fc1-112">Example 1</span></span>
```powershell
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group1' -Name 'Contoso01SFCluster' -Thumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A -Admin
```

<span data-ttu-id="89fc1-113">Эта команда добавит в кластер сертификат с препечаткой 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A, чтобы клиент может использовать сертификат как администратор для взаимодействия с кластером.</span><span class="sxs-lookup"><span data-stu-id="89fc1-113">This command will add the certificate with thumbprint '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster, so the client can use the certificate as admin to communicate with the cluster.</span></span>

### <span data-ttu-id="89fc1-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="89fc1-114">Example 2</span></span>
```
PS c:> Add-AzServiceFabricClientCertificate -ResourceGroupName 'Group2' -Name 'Contoso02SFCluster' -CommonName 'Contoso.com' -IssuerThumbprint 5F3660C715EBBDA31DB1FFDCF508302348DE8E7A
```

<span data-ttu-id="89fc1-115">Эта команда добавляет в кластер только для чтения клиентский сертификат с общим именем "Contoso.com", а препечатка выдачи — "5F3660C715EBBDA31DB1FFDCF508302348DE8E7A".</span><span class="sxs-lookup"><span data-stu-id="89fc1-115">This command will add a read only client certificate that's common name is 'Contoso.com' and issuer thumbprint is '5F3660C715EBBDA31DB1FFDCF508302348DE8E7A' to the cluster.</span></span>

## <span data-ttu-id="89fc1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89fc1-116">PARAMETERS</span></span>

### <span data-ttu-id="89fc1-117">-Администратор</span><span class="sxs-lookup"><span data-stu-id="89fc1-117">-Admin</span></span>
<span data-ttu-id="89fc1-118">Тип проверки подлинности клиента</span><span class="sxs-lookup"><span data-stu-id="89fc1-118">Client authentication type</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SingleUpdateWithThumbprint, SingleUpdateWithCommonName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89fc1-119">-AdminClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="89fc1-119">-AdminClientThumbprint</span></span>
<span data-ttu-id="89fc1-120">Эскиз "Указание сертификата клиента" с разрешением администратора</span><span class="sxs-lookup"><span data-stu-id="89fc1-120">Specify client certificate thumbprint which only has admin permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89fc1-121">-ClientCertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="89fc1-121">-ClientCertificateCommonName</span></span>
<span data-ttu-id="89fc1-122">Указание общего имени клиента, thumbprint-выдачи и типа проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="89fc1-122">Specify client common name , issuer thumbprint and authentication type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]
Parameter Sets: MultipleUpdatesWithCommonName
Aliases: CertCommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89fc1-123">-CommonName</span><span class="sxs-lookup"><span data-stu-id="89fc1-123">-CommonName</span></span>
<span data-ttu-id="89fc1-124">Указание общего имени сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="89fc1-124">Specify client certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89fc1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89fc1-125">-DefaultProfile</span></span>
<span data-ttu-id="89fc1-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89fc1-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89fc1-127">-IssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="89fc1-127">-IssuerThumbprint</span></span>
<span data-ttu-id="89fc1-128">Указание thumbprint of client certificate's issuer</span><span class="sxs-lookup"><span data-stu-id="89fc1-128">Specify thumbprint of client certificate's issuer</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithCommonName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89fc1-129">-Name</span><span class="sxs-lookup"><span data-stu-id="89fc1-129">-Name</span></span>
<span data-ttu-id="89fc1-130">Указание имени кластера</span><span class="sxs-lookup"><span data-stu-id="89fc1-130">Specify the name of the cluster</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89fc1-131">-ReadonlyClientThumbprint</span><span class="sxs-lookup"><span data-stu-id="89fc1-131">-ReadonlyClientThumbprint</span></span>
<span data-ttu-id="89fc1-132">Укажите эскиз сертификата клиента с разрешением только на чтение</span><span class="sxs-lookup"><span data-stu-id="89fc1-132">Specify client certificate thumbprint which only has read only permission</span></span>

```yaml
Type: System.String[]
Parameter Sets: MultipleUpdatesWithThumbprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89fc1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89fc1-133">-ResourceGroupName</span></span>
<span data-ttu-id="89fc1-134">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="89fc1-134">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="89fc1-135">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="89fc1-135">-Thumbprint</span></span>
<span data-ttu-id="89fc1-136">Укажите эскиз сертификата клиента</span><span class="sxs-lookup"><span data-stu-id="89fc1-136">Specify client certificate thumbprint</span></span>

```yaml
Type: System.String
Parameter Sets: SingleUpdateWithThumbprint
Aliases: ClientCertificateThumbprint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89fc1-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89fc1-137">-Confirm</span></span>
<span data-ttu-id="89fc1-138">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89fc1-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fc1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89fc1-139">-WhatIf</span></span>
<span data-ttu-id="89fc1-140">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89fc1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89fc1-141">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="89fc1-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89fc1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89fc1-142">CommonParameters</span></span>
<span data-ttu-id="89fc1-143">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89fc1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89fc1-144">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89fc1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89fc1-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89fc1-145">INPUTS</span></span>

### <span data-ttu-id="89fc1-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="89fc1-146">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="89fc1-147">System.String</span><span class="sxs-lookup"><span data-stu-id="89fc1-147">System.String</span></span>

### <span data-ttu-id="89fc1-148">System.String[]</span><span class="sxs-lookup"><span data-stu-id="89fc1-148">System.String[]</span></span>

### <span data-ttu-id="89fc1-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span><span class="sxs-lookup"><span data-stu-id="89fc1-149">Microsoft.Azure.Commands.ServiceFabric.Models.PSClientCertificateCommonName[]</span></span>

## <span data-ttu-id="89fc1-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89fc1-150">OUTPUTS</span></span>

### <span data-ttu-id="89fc1-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span><span class="sxs-lookup"><span data-stu-id="89fc1-151">Microsoft.Azure.Commands.ServiceFabric.Models.PSCluster</span></span>

## <span data-ttu-id="89fc1-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89fc1-152">NOTES</span></span>

## <span data-ttu-id="89fc1-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89fc1-153">RELATED LINKS</span></span>

[<span data-ttu-id="89fc1-154">Remove-AzServiceFabricClientCertificate</span><span class="sxs-lookup"><span data-stu-id="89fc1-154">Remove-AzServiceFabricClientCertificate</span></span>](./Remove-AzServiceFabricClientCertificate.md)
